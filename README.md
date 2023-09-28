# ox_gridsystem
gridsystem with ox_lib points



```
-- register Marker
TriggerEvent('ox_gridsystem:registerMarker', {

    name = 'a_unique_name_for_this_marker',

    pos = vector3(0.0, 0.0, 0.0),
    scale = vector3(1.5, 1.5, 1.5),

    control = 'E',
    type = 20,
    
    drawDistance = 5,
    interactDistance = 2,
    
    show3D  = true;
    msg = 'Press ~INPUT_CONTEXT~ to do something',

    shouldBob = true,
    shouldRotate = true,

    color = { r = 130, g = 120, b = 110 },

    action = function()
        print('This is executed when you press E in the marker')
    end,
    onEnter = function()
        print('This is executed when you enter a marker')
    end,
    onExit = function()
        print('This is executed when you eixit a marker')
    end,

    --For Custom Marker
    texture = "texture_name" or nil,  
    textureDict = "texture_dict" or nil,

    --For Marker only job (esx (1 and 2) or qbcore )
    permission = "police" or {"police","ambulance"},
    jobGrade = 0,
})

-- unregister Marker
TriggerEvent('ox_gridsystem:unregisterMarker', 'name_of_the_marker')


--gridsystem retro-compatibility (https://github.com/Profex1999/gridsystem)

-- register Marker
TriggerEvent('gridsystem:registerMarker', {

    name = 'a_unique_name_for_this_marker',

    pos = vector3(0.0, 0.0, 0.0),
    scale = vector3(1.5, 1.5, 1.5),

    control = 'E',
    type = 20,
    
    drawDistance = 5,
    interactDistance = 2,
    
    show3D  = true;
    msg = 'Press ~INPUT_CONTEXT~ to do something',

    shouldBob = true,
    shouldRotate = true,

    color = { r = 130, g = 120, b = 110 },

    action = function()
        print('This is executed when you press E in the marker')
    end,
    onEnter = function()
        print('This is executed when you enter a marker')
    end,
    onExit = function()
        print('This is executed when you eixit a marker')
    end,


    --For Custom Marker
    texture = "texture_name" or nil,  
    textureDict = "texture_dict" or nil,

    --For Marker only job (esx (1 and 2) or qbcore )
    permission = "police" or {"police","ambulance"},
    jobGrade = 0,
})

-- unregister Marker
TriggerEvent('gridsystem:unregisterMarker', 'name_of_the_marker')
```
