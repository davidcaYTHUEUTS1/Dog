local function A()
    if not game:IsLoaded()then 
        local l=Instance.new("Message",workspace);
        l.Text='Waiting game to loaded before scripts is getting executed by Xenon Hub';
        game.Loaded:Wait();
        l:Destroy();
        wait(15);
    end;
    
    local g=loadstring(game:HttpGet("https://androssy.net/TrashXenon/PepUiLib.lua"))();
    
    do local F=g.subs.Wait;
        local G;G=hookmetamethod(game,"__namecall",function(...)
            local N,i=(...),({select(2,...)});
            if tostring(getnamecallmethod())=="InvokeServer"and tostring(N)=="Skill"and i[1]=="Blocking "then 
                return;
            end;
            return G(...);
        end);
        local L=g:CreateWindow({Name="Xenon Hub Premium",Themeable={Info="Discord Server: discord.gg/xenonhub"}});
        local j=L:CreateTab({Name="General"});
        getgenv().DefaultSettings={
            Vex="0.0.0",
            Auto_Farm_Level=false,
            Ship_Max_Distance=1000,
            Auto_Farm_Ship=false,
            Auto_Farm_Ship_Cannon=false,
            Selected_Island="",
            Island_ESP=false,
            Teleport=false,
            Dungeon_Stop_At=25,
            Auto_Farm_Dungeon=false,
            Auto_Store_Fruit=false,
            Auto_Train_Buso_Haki=false,
            Auto_Finish_Mini=false,
            Selected_Weapons="Rifle",
            Safe_Modes=false,
            Hide_Name=true,
            Select_Stats={},
            Auto_Stats=false,
            WalkSpeed=16,
            JumpPower=50,
            No_CrashShip_Damage=false,
            Walk_On_Water=false,
            Inf_Dodge=false,
            Inf_Geppo=false,
            No_Fall_Damage=false,
            No_Drown=false,
            PS_Code="",
            PS_Rejoin=false,
            Full_Bright=false,
            No_Fog=false,
            Auto_Kick=false};
            getgenv().RefreshFile=function()
                local V="Xenon Hub Premium Scripts";
                local I="GPO_REWORK_"..game.Players.LocalPlayer.Name..".json";
                _G.Settings=game:service('HttpService'):JSONDecode(readfile(V.."/"..I));
                for H=1,2 do 
                    if _G.Settings.Vex~=getgenv().DefaultSettings.Vex then 
                        writefile(V.."/"..I,game:service('HttpService'):JSONEncode(getgenv().DefaultSettings));
                    else _G.Settings=game:service('HttpService'):JSONDecode(readfile(V.."/"..I));
                    end;
                end;
            end;
            local v="Xenon Hub Premium Scripts";
            local z="GPO_REWORK_"..game.Players.LocalPlayer.Name..".json";
            _G.Settings={};pcall(function()makefolder(tostring(v));
            end);
            if not pcall(function()readfile(v.."/"..z);end)then 
                writefile(v.."/"..z,game:service('HttpService'):JSONEncode(getgenv().DefaultSettings));
            end;
            local function B()
                task.spawn(function()
                    pcall(function()
                        writefile(v.."/"..z,game:service('HttpService'):JSONEncode(_G.Settings));
                    end);
                end);
            end;
            _G.Settings=game:service('HttpService'):JSONDecode(readfile(v.."/"..z));
            for H=1,2 do 
                if _G.Settings.Vex~=getgenv().DefaultSettings.Vex then RefreshFile();
                    print("loading lastest version.");
                else _G.Settings=game:service('HttpService'):JSONDecode(readfile(v.."/"..z));
                end;
            end;
            local b=j:CreateSection({Name="Auto Farm Level",Side='Left'});
            GetSubPrefix=function(d)
                local d=tostring(d):gsub(" ","");
                local M="";
                if#d==2 then 
                    local N=string.sub(d,#d,#d+1);
                    M=N=="1"and"st"or N=="2"and"nd"or N=="3"and"rd"or"th";
                end;
                return M;
            end;
            local E="%A, %B";
            local P=os.date(" %d",os.time());
            local Q=", %Y.";
            E=os.date(E,os.time())..P..GetSubPrefix(P)..os.date(Q,os.time());

            b:AddLabel({Text="Welcome To Xenon Hub Community"});b:AddLabel({Text=tostring(E)});

            b:AddToggle({Name="Auto Farm Level",Value=_G.Settings.Auto_Farm_Level,Locked=false,Callback=function(J)
                _G.Settings.Auto_Farm_Level=J;
                B();
            end});
            if keypress~=nil and keyrelease~=nil and firesignal~=nil then 
                btwthispassed=true;
            else game.Players.LocalPlayer:Kick("Missing Functions");
            end;
            repeat wait();
            until btwthispassed;
            getgenv().getClosestChest=function()
                local K=nil;
                local X=math.huge;
                for C,V in pairs(game:GetService("Workspace").Env:GetChildren())do 
                    if V.Name=="Part"and V:FindFirstChild("ClickDetector")then 
                        local M=(V.Position-game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude;
                        if M<X then K=V;
                            X=M;
                        end;
                    end;
                end;
                return K;
            end;
            getgenv().getClosestPlayer=function()
                local c=nil;
                local d=math.huge;
                local H={"Fishman Karate User","Yeti","Bandit Boss","Axe Hand Logan","Gravito"};
                for C,N in pairs(game:GetService("Workspace").NPCs:GetChildren())do 
                    if N.Name~=game.Players.LocalPlayer.Name and table.find(H,tostring(N.Name))then 
                        if N and N:FindFirstChildOfClass("Humanoid")and N:FindFirstChildOfClass("Humanoid").Health~=0 and N:FindFirstChild("HumanoidRootPart")and N:FindFirstChild("Head")and not N:FindFirstChild("QuestMark")then 
                            local w=(N.HumanoidRootPart.Position-game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude;
                            if w<d then 
                                c=N;
                                d=w;
                            end;
                        end;
                    end;
                end;
                return c;
            end;
            getgenv().ToTarget=function(c)
                pcall(function()
                    if game:GetService("ReplicatedStorage")["Stats"..game.Players.LocalPlayer.Name].Stats.JailTime.Value==0 then 
                        if not game.Players.LocalPlayer.PlayerGui:FindFirstChild("DEATHGUI")then 
                            if not game.Players.LocalPlayer.Character:FindFirstChild("Root")then 
                                local w=Instance.new("Part",game.Players.LocalPlayer.Character);
                                w.Size=Vector3.new(1,0.5,1);
                                w.Name="Root";w.Anchored=true;
                                w.Transparency=1;
                                w.CanCollide=false;
                                w.CFrame=game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame*CFrame.new(0,20,0);
                            end;
                            local N=(game.Players.LocalPlayer.Character.HumanoidRootPart.Position-c.Position).Magnitude;
                            local l=game:service("TweenService");local J=TweenInfo.new((c.Position-game.Players.LocalPlayer.Character.Root.Position).Magnitude/60,Enum.EasingStyle.Linear);
                            local d,I=pcall(function()
                                local V=l:Create(game.Players.LocalPlayer.Character.Root,J,{CFrame=c});
                                V:Play();
                            end);
                            if not d then 
                                return I;
                            end;
                            game.Players.LocalPlayer.Character.Root.CFrame=game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame;
                            if d and game.Players.LocalPlayer.Character:FindFirstChild("Root")then 
                                pcall(function()
                                    if(game.Players.LocalPlayer.Character.HumanoidRootPart.Position-c.Position).Magnitude>=20 then 
                                        spawn(function()
                                            pcall(function()
                                                if(game.Players.LocalPlayer.Character.Root.Position-game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude>150 then 
                                                    game.Players.LocalPlayer.Character.Root.CFrame=game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame;
                                                else game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame=game.Players.LocalPlayer.Character.Root.CFrame;
                                                end;
                                            end);
                                        end);
                                    elseif(game.Players.LocalPlayer.Character.HumanoidRootPart.Position-c.Position).Magnitude>=10 and(game.Players.LocalPlayer.Character.HumanoidRootPart.Position-c.Position).Magnitude<20 then 
                                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame=c;
                                    elseif(game.Players.LocalPlayer.Character.HumanoidRootPart.Position-c.Position).Magnitude<10 then 
                                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame=c;
                                    end;
                                end);
                            end;
                        end;
                    end;
                end);
            end;
            getgenv().ToTargetIsland=function(C)
                pcall(function()
                    if game:GetService("ReplicatedStorage")["Stats"..game.Players.LocalPlayer.Name].Stats.JailTime.Value==0 then 
                        if not game.Players.LocalPlayer.PlayerGui:FindFirstChild("DEATHGUI")then 
                            if not game.Players.LocalPlayer.Character:FindFirstChild("Root")then 
                                local V=Instance.new("Part",game.Players.LocalPlayer.Character);
                                V.Size=Vector3.new(1,0.5,1);
                                V.Name="Root";
                                V.Anchored=true;
                                V.Transparency=1;
                                V.CanCollide=false;
                                V.CFrame=game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame*CFrame.new(0,20,0);
                            end;
                            local D=(game.Players.LocalPlayer.Character.HumanoidRootPart.Position-C.Position).Magnitude;
                            local K=game:service("TweenService");
                            local I=TweenInfo.new((C.Position-game.Players.LocalPlayer.Character.Root.Position).Magnitude/60,Enum.EasingStyle.Linear);
                            local J,i=pcall(function()
                                local d=K:Create(game.Players.LocalPlayer.Character.Root,I,{CFrame=C});
                                d:Play();
                            end);
                            if not J then 
                                return i;
                            end;
                            game.Players.LocalPlayer.Character.Root.CFrame=game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame;
                            if J and game.Players.LocalPlayer.Character:FindFirstChild("Root")then 
                                pcall(function()
                                    if game.Players.LocalPlayer.Character.HumanoidRootPart.Position.y>=-1 then 
                                        game.Players.LocalPlayer.Character.Root.CFrame=game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame*CFrame.new(0,-4.085,0);
                                    end;
                                end);
                                pcall(function()
                                    if(game.Players.LocalPlayer.Character.HumanoidRootPart.Position-C.Position).Magnitude>=20 then 
                                        spawn(function()
                                            pcall(function()
                                                if(game.Players.LocalPlayer.Character.Root.Position-game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude>150 then 
                                                    game.Players.LocalPlayer.Character.Root.CFrame=game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame;
                                                else game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame=game.Players.LocalPlayer.Character.Root.CFrame;
                                                end;
                                            end);
                                        end);
                                    elseif(game.Players.LocalPlayer.Character.HumanoidRootPart.Position-C.Position).Magnitude>=10 and(game.Players.LocalPlayer.Character.HumanoidRootPart.Position-C.Position).Magnitude<20 then 
                                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame=C;
                                    elseif(game.Players.LocalPlayer.Character.HumanoidRootPart.Position-C.Position).Magnitude<10 then 
                                        J=false;
                                    end;
                                end);
                            end;
                        end;
                    end;
                end);
            end;
            
            getgenv().IsBuso=function()
                if game:GetService("ReplicatedStorage")["Stats"..game.Players.LocalPlayer.Name].Stats.JailTime.Value==0 then 
                    if not game.Players.LocalPlayer.PlayerGui:FindFirstChild("DEATHGUI")then 
                        for D,M in pairs(game.Players.LocalPlayer.Character:GetChildren())do 
                            if M.Name:find("Buso")then
                                return true;
                            end;
                        end;
                    end;
                end;
                return false;
            end;
            getgenv().Reload=function()
                pcall(function()
                    if game:GetService("ReplicatedStorage")["Stats"..game.Players.LocalPlayer.Name].Stats.JailTime.Value==0 then 
                        if not game.Players.LocalPlayer.PlayerGui:FindFirstChild("DEATHGUI")then 
                            if tostring(game:GetService("Players").LocalPlayer.Character.Humanoid.FloorMaterial)~="Air"then 
                                game:GetService("ReplicatedStorage").Events.CIcklcon.gunFunctions:InvokeServer("reload",{["Gun"]="Rifle"});
                            end;
                        end;
                    end;
                end);
            end;
            getgenv().ShootAt=function(S)if game:GetService("ReplicatedStorage")["Stats"..game.Players.LocalPlayer.Name].Stats.JailTime.Value==0 then 
                if not game.Players.LocalPlayer.PlayerGui:FindFirstChild("DEATHGUI")then 
                local u={[1]="fire",[2]={["Start"]=CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.Position+Vector3.new(0,5,5),game.Players.LocalPlayer.Character.HumanoidRootPart.Position+Vector3.new(0,5,5)),["Gun"]="Rifle",["joe"]="true",["Position"]=S}};
                game:GetService("ReplicatedStorage").Events.CIcklcon:FireServer(unpack(u));
            end;
        end;
    end;
    getgenv().IsSkill=function()num=0;
        if not game:GetService("Workspace").NPCs:FindFirstChild("Gravito")then 
            return num;
        end;
        for C,K in pairs(game:GetService("Workspace").Effects:GetChildren())do 
            if K.Name:find("Rings")then 
                num=3;
            end;
        end;
        return num;
    end;
    getgenv().getClosestShipMobs_1=function()
        local R=nil;local D=math.huge;
        local X={"Marine Captain","Pirate Captain"};
        for I,l in pairs(game:GetService("Workspace").NPCs:GetChildren())do 
            if l.Name~=game.Players.LocalPlayer.Name and table.find(X,tostring(l.Name))then 
                if l and l:FindFirstChildOfClass("Humanoid")and l:FindFirstChildOfClass("Humanoid").Health~=0 and l:FindFirstChild("HumanoidRootPart")and l:FindFirstChild("Head")and not l:FindFirstChild("QuestMark")and(l.HumanoidRootPart.Position-getgenv().Old_Position.Position).magnitude<=tonumber(_G.Settings.Auto_Farm_Ship_Distance)then 
                    if _G.Settings.Auto_Farm_Ship_Ignore_Galleons then 
                        if l:FindFirstChild("assignedShip")and l.assignedShip.Value~="Marine's Galleon"or l.assignedShip.Value~="Galleon"then 
                            local W=(l.HumanoidRootPart.Position-game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude;
                            if W<D then 
                                R=l;
                                D=W;
                            end;
                        end;
                    else local W=(l.HumanoidRootPart.Position-game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude;
                        if W<D then 
                            R=l;
                            D=W;
                        end;
                    end;
                end;
            end;
        end;
        return R;
    end;
    getgenv().getClosestShipMobs_2=function()
        local i=nil;local V=math.huge;
        local W={"Marine Cannoneer","Pirate Cannoneer"};
        for I,u in pairs(game:GetService("Workspace").NPCs:GetChildren())do 
            if u.Name~=game.Players.LocalPlayer.Name and table.find(W,tostring(u.Name))then if u and u:FindFirstChildOfClass("Humanoid")and u:FindFirstChildOfClass("Humanoid").Health~=0 and u:FindFirstChild("HumanoidRootPart")and u:FindFirstChild("Head")and not u:FindFirstChild("QuestMark")and(u.HumanoidRootPart.Position-getgenv().Old_Position.Position).magnitude<=tonumber(_G.Settings.Ship_Max_Distance)then 
                if _G.Settings.Auto_Farm_Ship_Ignore_Galleons then 
                    if u:FindFirstChild("assignedShip")and u.assignedShip.Value~="Marine's Galleon"or u.assignedShip.Value~="Galleon"then 
                        local p=(u.HumanoidRootPart.Position-game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude;
                        if p<V then i=u;
                            V=p;
                        end;
                    end;
                else local M=(u.HumanoidRootPart.Position-game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude;
                    if M<V then 
                        i=u;
                        V=M;
                    end;
                end;
            end;
        end;
    end;
    return i;
end;
getgenv().ToTarget2=function(W)
    pcall(function()
        if game:GetService("ReplicatedStorage")["Stats"..game.Players.LocalPlayer.Name].Stats.JailTime.Value==0 then 
            if not game.Players.LocalPlayer.PlayerGui:FindFirstChild("DEATHGUI")then 
                if not game.Players.LocalPlayer.Character:FindFirstChild("Root")then 
                    local K=Instance.new("Part",game.Players.LocalPlayer.Character);
                    K.Size=Vector3.new(1,0.5,1);
                    K.Name="Root";
                    K.Anchored=true;
                    K.Transparency=1;
                    K.CanCollide=false;
                    K.CFrame=game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame*CFrame.new(0,20,0);
                end;
                local p=(game.Players.LocalPlayer.Character.HumanoidRootPart.Position-W.Position).Magnitude;
                local D=game:service("TweenService");
                local i=TweenInfo.new((W.Position-game.Players.LocalPlayer.Character.Root.Position).Magnitude/60,Enum.EasingStyle.Linear);
                local C,w=pcall(function()
                    local V=D:Create(game.Players.LocalPlayer.Character.Root,i,{CFrame=W});
                    V:Play();
                end);
                if not C then 
                    return w;
                end;
                game.Players.LocalPlayer.Character.Root.CFrame=game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame;
                if C and game.Players.LocalPlayer.Character:FindFirstChild("Root")then 
                    pcall(function()
                        if(game.Players.LocalPlayer.Character.HumanoidRootPart.Position-W.Position).Magnitude>=20 then 
                            spawn(function()
                                pcall(function()
                                    if(game.Players.LocalPlayer.Character.Root.Position-game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude>150 then 
                                        game.Players.LocalPlayer.Character.Root.CFrame=game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame;
                                    else game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame=game.Players.LocalPlayer.Character.Root.CFrame;
                                    end;
                                end);
                            end);
                        elseif(game.Players.LocalPlayer.Character.HumanoidRootPart.Position-W.Position).Magnitude>=10 and(game.Players.LocalPlayer.Character.HumanoidRootPart.Position-W.Position).Magnitude<20 then 
                            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame=W;
                        elseif(game.Players.LocalPlayer.Character.HumanoidRootPart.Position-W.Position).Magnitude<10 then 
                            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame=W;
                        end;
                    end);
                end;
            end;
        end;
    end);
end;
getgenv().Types=math.random(1,4);
task.spawn(function()
    repeat wait();
    until _G.Settings.Auto_Farm_Level;
    print("Auto Farm Level Activated");
    while true do wait();
        if _G.Settings.Auto_Farm_Level then 
            task.spawn(function()
                pcall(function()
                    if game:GetService("ReplicatedStorage")["Stats"..game.Players.LocalPlayer.Name].Stats.DF.Value~=""then 
                        game:GetService("ReplicatedStorage")["Stats"..game.Players.LocalPlayer.Name].Stats.DF.Value="";
                    end;
                    if game:GetService("ReplicatedStorage")["Stats"..game.Players.LocalPlayer.Name].Stats.Level.Value>=425 then 
                    else a=game:GetService("ReplicatedStorage")["Stats"..game.Players.LocalPlayer.Name].Inventory.Inventory.Value;
                        if game:GetService("ReplicatedStorage")["Stats"..game.Players.LocalPlayer.Name].Stats.Level.Value>=325 and not string.find(a,"World Scroll")then if(Vector3.new(7928,-2153,-17138)-game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude<=2500 then 
                            ToTarget(CFrame.new(8585,-2136,-17087));
                        else if game:GetService("Workspace").Effects:FindFirstChild("World Scroll")then 
                            if game.Players.LocalPlayer:DistanceFromCharacter(game:GetService("Workspace").Effects:FindFirstChild("World Scroll").Position)<=200 then 
                                ToTarget(game:GetService("Workspace").Effects:FindFirstChild("World Scroll").CFrame);
                                if game.Players.LocalPlayer:DistanceFromCharacter(game:GetService("Workspace").Effects:FindFirstChild("World Scroll").Position)<=20 then 
                                    game:GetService("VirtualInputManager"):SendKeyEvent(true,"LeftAlt",false,game);
                                end;
                            else ToTargetIsland(game:GetService("Workspace").Effects:FindFirstChild("World Scroll").CFrame);
                            end;
                        else ToTargetIsland(CFrame.new(-12179,-4.085,-18545));
                        end;
                    end;
                else a=game:GetService("ReplicatedStorage")["Stats"..game.Players.LocalPlayer.Name].Inventory.Inventory.Value;
                    if string.find(a,"Rifle")then 
                        if not game.Players.LocalPlayer.Backpack:FindFirstChild("Rifle")and not game.Players.LocalPlayer.Character:FindFirstChild("Rifle")then 
                            local c={[1]="equip",[2]="Rifle"};
                            game:GetService("ReplicatedStorage").Events.Tools:InvokeServer(unpack(c));
                            wait(1);
                        else if game:GetService("ReplicatedStorage")["Stats"..game.Players.LocalPlayer.Name].Stats.BusoMastery.Value==0 and game:GetService("ReplicatedStorage")["Stats"..game.Players.LocalPlayer.Name].Stats.Level.Value>=150 and game:GetService("ReplicatedStorage")["Stats"..game.Players.LocalPlayer.Name].Stats.Peli.Value>=25000 or game:GetService("ReplicatedStorage")["Stats"..game.Players.LocalPlayer.Name].Stats.BusoMastery.Value==0 and game:GetService("ReplicatedStorage")["Stats"..game.Players.LocalPlayer.Name].Stats.Level.Value>=150 and game:GetService("ReplicatedStorage")["Stats"..game.Players.LocalPlayer.Name].Quest.CurrentQuest.Value=="Road to Armament"then if(Vector3.new(7928,-2153,-17138)-game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude<2500 then 
                            ToTarget(CFrame.new(8585,-2136,-17087));
                        else if not game:GetService("Workspace").NPCs:FindFirstChild("Ray")then 
                            ToTargetIsland(CFrame.new(-6700,-4.085,2099));
                        else if game:GetService("ReplicatedStorage")["Stats"..game.Players.LocalPlayer.Name].Quest.CurrentQuest.Value=="Road to Armament"then 
                            ToTarget(CFrame.new(-6700,53,2099));
                        else ToTarget(game:GetService("Workspace").NPCs:FindFirstChild("Ray").PrimaryPart.CFrame);
                            if game.Players.LocalPlayer:DistanceFromCharacter(game:GetService("Workspace").NPCs:FindFirstChild("Ray").PrimaryPart.Position)<=20 then 
                                game:GetService("VirtualInputManager"):SendKeyEvent(true,"T",false,game);
                                if game:GetService("Players").LocalPlayer.PlayerGui:FindFirstChild("NPCCHAT")then 
                                    firesignal(game:GetService("Players").LocalPlayer.PlayerGui.NPCCHAT.Frame.go.MouseButton1Click);
                                end;
                            end;
                        end;
                    end;
                end;
            else if(Vector3.new(7928,-2153,-17138)-game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude<2500 then 
                if game:GetService("ReplicatedStorage")["Stats"..game.Players.LocalPlayer.Name].Stats.SpawnPoint.Value=="Fishman Island"then 
                    if game:GetService("ReplicatedStorage")["Stats"..game.Players.LocalPlayer.Name].Quest.CurrentQuest.Value=="None"and game:GetService("ReplicatedStorage")["Stats"..game.Players.LocalPlayer.Name].Stats.Level.Value>=190 then 
                        if game:GetService("Players").LocalPlayer.QuestCD.Value==false then 
                            ToTarget(CFrame.new(7731,-2176,-17222));
                            if game.Players.LocalPlayer:DistanceFromCharacter(Vector3.new(7731,-2176,-17222))<=20 then 
                                game:GetService("VirtualInputManager"):SendKeyEvent(true,"T",false,game);
                                if game:GetService("Players").LocalPlayer.PlayerGui:FindFirstChild("NPCCHAT")then 
                                    firesignal(game:GetService("Players").LocalPlayer.PlayerGui.NPCCHAT.Frame.go.MouseButton1Click);
                                end;
                            end;
                        else if _G.Settings.Safe_Modes then 
                            ToTarget(CFrame.new(7854,-2177,-17319));
                        else ToTarget(CFrame.new(7489,-2179,-17296));
                        end;
                    end;
                else if game:GetService("ReplicatedStorage")["Stats"..game.Players.LocalPlayer.Name].Quest.CurrentQuest.Value=="Road to Armament"then 
                    ToTarget(CFrame.new(-6700,53,2099));
                else if _G.Settings.Safe_Modes then 
                    ToTarget(CFrame.new(7854,-2177,-17319));
                else ToTarget(CFrame.new(7489,-2179,-17296));
                end;
            end;
        end;
    else ToTarget(CFrame.new(7976,-2153,-17073));
        if workspace.NPCs:FindFirstChild("Robo")then 
            game:GetService("VirtualInputManager"):SendKeyEvent(true,"T",false,game);
            if game:GetService("Players").LocalPlayer.PlayerGui:FindFirstChild("NPCCHAT")then 
                firesignal(game:GetService("Players").LocalPlayer.PlayerGui.NPCCHAT.Frame.go.MouseButton1Click);
            end;
        end;
    end;
else if not game:GetService("Workspace").NPCs:FindFirstChild("Brad")then 
    ToTargetIsland(CFrame.new(5676,-4.085,-16460));
else ToTarget(CFrame.new(5639.87,-92.762,-16611.5));
end;
end;
end;
end;
else if game:GetService("ReplicatedStorage")["Stats"..game.Players.LocalPlayer.Name].Stats.Peli.Value>=300 then 
    if game.Players.LocalPlayer:DistanceFromCharacter(Vector3.new(1003,9,1132))<=500 then 
        ToTarget(CFrame.new(1003,9,1132));
        if game.Players.LocalPlayer:DistanceFromCharacter(Vector3.new(1003,9,1132))<=20 then 
            fireclickdetector(game:GetService("Workspace").BuyableItems.Rifle.ShopPart.ClickDetector);
            if game:GetService("Players").LocalPlayer.PlayerGui:FindFirstChild("NPCCHAT")then 
                firesignal(game:GetService("Players").LocalPlayer.PlayerGui.NPCCHAT.Frame.go.MouseButton1Click);
            end;
        end;
    else ToTargetIsland(CFrame.new(1003,9,1132));
    end;
else Chest=getClosestChest();
    if Chest~=nil then 
        if game.Players.LocalPlayer:DistanceFromCharacter(Chest.Position)<=100 then 
            ToTarget(Chest.CFrame);
            if game.Players.LocalPlayer:DistanceFromCharacter(Chest.Position)<=10 and Chest:FindFirstChild("ClickDetector")then 
                fireclickdetector(Chest:FindFirstChild("ClickDetector"));
            end;
        else ToTargetIsland(Chest.CFrame);
        end;
    end;
end;
end;
end;
end;
end);
end);
end;
end;
end);

task.spawn(function()
    repeat wait();
    until _G.Settings.Auto_Farm_Level;
    while true do wait();
        if _G.Settings.Auto_Farm_Level then 
        if game.Players.LocalPlayer.Character:FindFirstChild("Rifle")then 
            Reload();
        end;
    end;
end;
end);

task.spawn(function()
    repeat wait();
    until _G.Settings.Auto_Farm_Level;
    while true do wait();
        if _G.Settings.Auto_Farm_Level then 
            getgenv().Mobs=getClosestPlayer();
            if game.Players.LocalPlayer.Character:FindFirstChild("Rifle")then 
                if Mobs~=nil and Mobs:FindFirstChild("Head")then 
                    ShootAt(Mobs:FindFirstChild("Head").Position);
                end;
            elseif not game.Players.LocalPlayer.Character:FindFirstChild("Rifle")then 
                if game.Players.LocalPlayer.Backpack:FindFirstChild("Rifle")then 
                    game.Players.LocalPlayer.Character.Humanoid:EquipTool(game.Players.LocalPlayer.Backpack:FindFirstChild("Rifle"));
                end;
            end;
        end;
    end;
end);

task.spawn(function()
    repeat wait();
    until _G.Settings.Auto_Farm_Level;
    while true do wait(1);
        if _G.Settings.Auto_Farm_Level then 
            if game:GetService("ReplicatedStorage")["Stats"..game.Players.LocalPlayer.Name].Stats.JailTime.Value==0 then 
                if not game.Players.LocalPlayer.PlayerGui:FindFirstChild("DEATHGUI")then 
                    if game:GetService("ReplicatedStorage")["Stats"..game.Players.LocalPlayer.Name].Stats.SkillPoints.Value~=0 then 
                        if game:GetService("ReplicatedStorage")["Stats"..game.Players.LocalPlayer.Name].Stats.GunMastery.Value<650 then 
                            local M={[1]="GunMastery",[3]=3};game:GetService("ReplicatedStorage").Events.stats:FireServer(unpack(M));
                        end;
                    end;
                end;
            end;
        end;
    end;
end);

local s=j:CreateSection({Name="Auto Farm Ship",Side='Left'});

s:AddSlider({Name="Ship's Max Distance",Min=0,Max=2000,Value=_G.Settings.Ship_Max_Distance,Callback=function(C,D)
    _G.Settings.Ship_Max_Distance=C;
    B();
end});

s:AddToggle({Name="Enabled",Value=_G.Settings.Auto_Farm_Ship,Locked=false,Callback=function(w)
    _G.Settings.Auto_Farm_Ship=w;
    B();
end});

s:AddToggle({Name="Kill Cannoneers",Value=_G.Settings.Auto_Farm_Ship_Cannon,Locked=false,Callback=function(c)
    _G.Settings.Auto_Farm_Ship_Cannon=c;
    B();
end});

task.spawn(function()
    repeat wait();
    until _G.Settings.Auto_Farm_Ship;
    while true do wait();
        if _G.Settings.Auto_Farm_Ship then 
            local i=getClosestShipMobs_1();
            if i~=nil then 
                repeat wait();
                    task.spawn(function()
                        if game.Players.LocalPlayer:DistanceFromCharacter(i:FindFirstChild("HumanoidRootPart").CFrame.Position)<=20 then 
                            ToTarget2(i:FindFirstChild("HumanoidRootPart").CFrame*CFrame.new(0,0,2));
                            if game.Players.LocalPlayer.Backpack:FindFirstChild("BlackLeg")then 
                                game.Players.LocalPlayer.Character.Humanoid:EquipTool(game.Players.LocalPlayer.Backpack:FindFirstChild("BlackLeg"));
                            end;
                            if game.Players.LocalPlayer.Character:FindFirstChild("BlackLeg")then 
                                getgenv().Punch();
                            end;
                            if not game.Players.LocalPlayer.Character:FindFirstChild("Value")then 
                                game:GetService("ReplicatedStorage").Events.Skill:InvokeServer("Party Table Kick Course");
                            end;
                        else ToTargetIsland(i:FindFirstChild("HumanoidRootPart").CFrame);
                        end;
                    end);
                until not i or i.Humanoid==nil or i.Humanoid.Health==0 or i.Parent~=game:GetService("Workspace").NPCs or not _G.Settings.Auto_Farm_Ship;
            else if _G.Settings.Auto_Farm_Ship_Cannon then 
                local w=getClosestShipMobs_2();
                if w~=nil then repeat wait();
                    task.spawn(function()
                        if game.Players.LocalPlayer:DistanceFromCharacter(w:FindFirstChild("HumanoidRootPart").CFrame.Position)<=20 then 
                            ToTarget2(w:FindFirstChild("HumanoidRootPart").CFrame);
                            if game.Players.LocalPlayer.Backpack:FindFirstChild("BlackLeg")then 
                                game.Players.LocalPlayer.Character.Humanoid:EquipTool(game.Players.LocalPlayer.Backpack:FindFirstChild("BlackLeg"));
                            end;
                            if game.Players.LocalPlayer.Character:FindFirstChild("BlackLeg")then 
                                getgenv().Punch();
                            end;
                            if not game.Players.LocalPlayer.Character:FindFirstChild("Value")then 
                                game:GetService("ReplicatedStorage").Events.Skill:InvokeServer("Party Table Kick Course");
                            end;
                        else ToTargetIsland(w:FindFirstChild("HumanoidRootPart").CFrame);
                        end;
                    end);
                until not w or w.Humanoid==nil or w.Humanoid.Health==0 or w.Parent~=game:GetService("Workspace").NPCs or getClosestShipMobs_1()~=nil or not _G.Settings.Auto_Farm_Ship;
            else if game:GetService("Workspace").Ships:FindFirstChild(game.Players.LocalPlayer.Name.."Ship")then 
                if game.Players.LocalPlayer:DistanceFromCharacter(game:GetService("Workspace").Ships:FindFirstChild(game.Players.LocalPlayer.Name.."Ship").PrimaryPart.CFrame.Position)<=50 then 
                    ToTarget2(getgenv().Old_Position);
                else ToTargetIsland(getgenv().Old_Position);
                end;
            else if game.Players.LocalPlayer:DistanceFromCharacter(getgenv().Old_Position.Position)<=10 then 
                wait(5);
                game:GetService("ReplicatedStorage").Events.ShipEvents.Spawn:InvokeServer("true");
            else ToTargetIsland(getgenv().Old_Position);
            end;
        end;
    end;
else if game:GetService("Workspace").Ships:FindFirstChild(game.Players.LocalPlayer.Name.."Ship")then 
    if game.Players.LocalPlayer:DistanceFromCharacter(game:GetService("Workspace").Ships:FindFirstChild(game.Players.LocalPlayer.Name.."Ship").PrimaryPart.CFrame.Position)<=50 then 
        ToTarget2(getgenv().Old_Position);
    else ToTargetIsland(getgenv().Old_Position);
    end;
else if game.Players.LocalPlayer:DistanceFromCharacter(getgenv().Old_Position.Position)<=10 then 
    game:GetService("ReplicatedStorage").Events.ShipEvents.Spawn:InvokeServer("true");
    wait(5);
else ToTargetIsland(getgenv().Old_Position);
end;
end;
end;
end;
end;
end;
end);
if game.PlaceId~=1730877806 and game.PlaceId~=6360478118 then 
    task.spawn(function()
        repeat wait();
        until _G.Settings.No_CrashShip_Damage or _G.Settings.Walk_On_Water or _G.Settings.Inf_Dodge or _G.Settings.Inf_Geppo or _G.Settings.No_Fall_Damage or _G.Settings.No_Drown;
        print("Enabled Misc Functions");
        local X=nil;
        X=hookfunction(getrawmetatable(game).__namecall,newcclosure(function(R,...)
            local u=getnamecallmethod();
            local l={...};
            if R.Name=="FallDmg"and _G.Settings.No_Fall_Damage==true then 
                return;
            end;
            if R.Name=="takestam"and _G.Settings.Inf_Dodge==true then return;end;if R.Name=="swim"and l[1]=="drown"and _G.Settings.No_Drown==true then 
                return;
            end;
            if R.Name=="Rough"and _G.Settings.No_CrashShip_Damage==true then 
                return;
            end;
            if R.Name=="Skill"and l[1]=='Geppo'and _G.Settings.Inf_Geppo==true or R.Name=="Skill"and l[1]=='Sky Walk'and _G.Settings.Inf_Geppo==true then 
                return;
            end;
            return X(R,...);
        end));
    end);
    task.spawn(function()
        repeat wait();
        until _G.Settings.No_Drown;
        print("Enabled No Drowns");
        hookfunction(game:GetService("ReplicatedStorage").Events.swim.FireServer,function()
            if _G.Settings.No_Drown then 
                return;
            end;
        end);
    end);
end;

if game.PlaceId~=1730877806 and game.PlaceId~=6360478118 then 
    getgenv().Name_Island_Collect=function()
        All_Island={};
        local D=tostring(name);
        for d,W in pairs(getrenv()._G.RenderCache:GetChildren())do 
            if W:FindFirstChild("SpawnPoint")then 
                table.insert(All_Island,W.Name);
            end;
        end;
        return All_Island;
    end;
    getgenv().All_Island=Name_Island_Collect();
    local p={};
    getgenv().getislandcord=function(M)
        local H=tostring(M);
        for l,N in pairs(getrenv()._G.RenderCache:GetChildren())do 
            if N.Name==H and N:FindFirstChild("SpawnPoint")then return N.SpawnPoint;
            elseif N.Name==H and not N:FindFirstChild("SpawnPoint")and N:FindFirstChildOfClass("Part")then 
                return N:FindFirstChildOfClass("Part");
            end;
        end;
        for C,S in pairs(workspace.Islands:GetChildren())do 
            if S.Name==H and S:FindFirstChild("SpawnPoint")then 
                return S.SpawnPoint;
            elseif S.Name==H and not S:FindFirstChild("SpawnPoint")and S:FindFirstChildOfClass("Part")then 
                return S:FindFirstChildOfClass("Part");
            end;
        end;
    end;
    pcall(function()
        for W,R in pairs(game:GetService("Workspace").Islands:GetChildren())do 
            if not table.find(getgenv().All_Island,R.Name)then table.insert(getgenv().All_Island,R.Name);
            end;
        end;
    end);
    pcall(function()
        for u,M in pairs(All_Island)do 
            p[M]=getislandcord(M);
        end;
    end);
    local K=j:CreateSection({Name="Island",Side='Left'});
    K:AddDropdown({Name="Select Island",Value=_G.Settings.Selected_Island,List=getgenv().All_Island,Callback=function(D,i)
        _G.Settings.Selected_Island=D;
        B();
    end});
    K:AddToggle({Name="Island ESP",Value=_G.Settings.Island_ESP,Locked=false,Callback=function(u)
        _G.Settings.Island_ESP=u;
        B();
    end});
    K:AddToggle({Name="Teleport",Value=_G.Settings.Teleport,Locked=false,Callback=function(w)
        _G.Settings.Teleport=w;
        B();
    end});
    task.spawn(function()
        repeat wait();
        until _G.Settings.Teleport and _G.Settings.Selected_Island~=nil;while true do wait();
            if _G.Settings.Teleport and _G.Settings.Selected_Island~=nil then 
                if(Vector3.new(7928,-2153,-17138)-game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude<2500 and _G.Settings.Selected_Island~="Fishman Island"then 
                    ToTarget(CFrame.new(8585,-2136,-17087));
                else Island=getislandcord(tostring(_G.Settings.Selected_Island));
                    if game.Players.LocalPlayer:DistanceFromCharacter(Island.CFrame.Position)<=20 then 
                        ToTarget(Island.CFrame);
                    else ToTargetIsland(Island.CFrame);
                    end;
                end;
            end;
        end;
    end);
    local X=workspace.CurrentCamera;
    function DrawESP(M,H)
        local C,d=X:WorldToViewportPoint(H.Position);
        local c=Drawing.new("Text");
        c.Color=Color3.fromRGB(0,255,0);
        c.Position=Vector2.new(C.x,C.y);
        c.Size=18;c.Outline=true;
        c.Center=true;
        c.Visible=true;
        game:GetService("RunService").Stepped:connect(function()
            if _G.Settings.Island_ESP then 
                local J,S=X:WorldToScreenPoint(H.Position);
                if H~=nil then 
                    c.Position=Vector2.new(J.x,J.y);
                    c.Text=M.." \n Distance: ["..tostring(math.round(game.Players.LocalPlayer:DistanceFromCharacter(H.Position))).."]";
                end;
                if S then 
                    c.Visible=true;
                else c.Visible=false;
                end;
            else c.Visible=false;
            end;
        end);
    end;
    for C,V in pairs(p)do 
        if V then pcall(function()
            DrawESP(C,V);
        end);
    end;
end;
end;
local k=j:CreateSection({Name="Dungeons",Side='Left'});
k:AddSlider({Name="Dungeon Stop At",Min=25,Max=50,Value=_G.Settings.Dungeon_Stop_At,Callback=function(c,C)
    _G.Settings.Dungeon_Stop_At=c;
    B();
end});
k:AddToggle({Name="Auto Farm Dungeons",Value=_G.Settings.Auto_Farm_Dungeon,Locked=false,Callback=function(u)
    _G.Settings.Auto_Farm_Dungeon=u;
    B();
end});
getgenv().Click_Tables={["Remotes"]=nil,["M1"]=nil,["M2"]=false};
getgenv().getRemote=function()
    for R,S in next,getgc()do 
        if type(S)=='function'and getfenv(S).script==game:GetService("Players").LocalPlayer.Backpack:FindFirstChild('MeleeScript')then 
            if pcall(function()getconstant(S,85);end)==true then 
                return S;end;end;end;return false;
            end;
            getgenv().Punch=function()
                if type(Click_Tables.Remotes)=='function'then 
                    Click_Tables.M1=game:GetService("UserInputService"):GetGamepadState(Enum.UserInputType.Gamepad1)[1];
                    Click_Tables.M1.UserInputType=Enum.UserInputType.MouseButton1;
                    Click_Tables.Remotes(Click_Tables.M1,Click_Tables.M2);
                else if not game:GetService("Workspace").Ragdolls:FindFirstChild(game.Players.LocalPlayer.Name)then 
                    if game.Players.LocalPlayer.Character:FindFirstChild("BlackLeg")then 
                        wait(2);
                        if not game.Players.LocalPlayer:FindFirstChild("DEATHGUI")then 
                            if Click_Tables.Remotes==nil then 
                                Click_Tables.Remotes=getRemote();
                                Click_Tables.Remotes=getRemote();
                                print("rendering!");
                            end;
                        end;
                    end;
                end;
            end;
        end;
        game.Players.LocalPlayer.CharacterAdded:Connect(function(V)V:WaitForChild("Humanoid",1);
            V:WaitForChild("Humanoid").Died:Connect(function()Click_Tables.Remotes=nil;
            end);
        end);
        game.Players.LocalPlayer.Character:WaitForChild("Humanoid").Died:Connect(function()
            Click_Tables.Remotes=nil;
        end);
        task.spawn(function()
            repeat wait();
            until _G.Settings.Auto_Farm_Dungeon;
            while true do wait();
                if _G.Settings.Auto_Farm_Dungeon then 
                    if game.PlaceId==1730877806 then 
                        game:GetService("ReplicatedStorage").Events.playgame:FireServer("arena");
                    elseif game.PlaceId==6360478118 then 
                        game:GetService("ReplicatedStorage").Events.Queue:InvokeServer("Dungeon");
                    elseif game.PlaceId==3978370137 then 
                        if game.Players.LocalPlayer.PlayerGui.Matchmake.TextLabel.Text~="GAME OVER"then 
                            if game:GetService("Workspace").PlayerCharacters:FindFirstChild(game.Players.LocalPlayer.Name.."'s Main Body")then 
                                for S,c in pairs(game:GetService("Workspace").NPCs:GetChildren())do 
                                    if c:FindFirstChild("Humanoid")then 
                                        repeat wait();
                                        task.spawn(function()
                                            if game:GetService("ReplicatedStorage").Matchinfo.wave.Value<tonumber(_G.Settings.Dungeon_Stop_At)then 
                                                if game:GetService("Workspace").PlayerCharacters:FindFirstChild(game.Players.LocalPlayer.Name.."'s Main Body")then 
                                                    local u=game:GetService("Players").LocalPlayer;
                                                    if game.Players.LocalPlayer.Backpack:FindFirstChild("BlackLeg")then 
                                                        game.Players.LocalPlayer.Character.Humanoid:EquipTool(game.Players.LocalPlayer.Backpack:FindFirstChild("BlackLeg"));
                                                    end;
                                                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame=c.HumanoidRootPart.CFrame*CFrame.new(0,0,-3);
                                                    local C=game.Players.LocalPlayer.Character;
                                                        C.HumanoidRootPart.CFrame=C.HumanoidRootPart.CFrame*CFrame.Angles(0,math.rad(180),0);
                                                        if not game.Players.LocalPlayer.Character:FindFirstChild("Value")and game.Players.LocalPlayer.Backpack:FindFirstChild("BlackLeg")then end;pcall(function()getgenv().Punch();end);else if game:GetService("Workspace").Islands:FindFirstChild("Tropical Island")then 
                                                            if game.Players.LocalPlayer:DistanceFromCharacter(Vector3.new(747,218,342))<=5 then 
                                                                if game.Players.LocalPlayer.Backpack:FindFirstChild("Horo-Horo")then 
                                                                    game.Players.LocalPlayer.Character.Humanoid:EquipTool(game.Players.LocalPlayer.Backpack:FindFirstChild("Horo-Horo"));
                                                                elseif game.Players.LocalPlayer.Character:FindFirstChild("Horo-Horo")then 
                                                                    if not game:GetService("Workspace").Ragdolls:FindFirstChild(game.Players.LocalPlayer.Name)then 
                                                                        repeat wait(1);
                                                                            if not game:GetService("Workspace").PlayerCharacters:FindFirstChild(game.Players.LocalPlayer.Name.."'s Main Body")then 
                                                                                game:GetService("VirtualInputManager"):SendKeyEvent(true,"T",false,game);
                                                                            end;
                                                                        until game:GetService("Workspace").PlayerCharacters:FindFirstChild(game.Players.LocalPlayer.Name.."'s Main Body")or not _G.Settings.Auto_Farm_Dungeon;
                                                                        wait(4);
                                                                    end;
                                                                end;
                                                            else ToTarget(CFrame.new(747,218,342));
                                                            end;
                                                        elseif game:GetService("Workspace").Islands:FindFirstChild("Sky Islands")then 
                                                            if game.Players.LocalPlayer:DistanceFromCharacter(Vector3.new(-908,131,-154))<=5 then 
                                                                if game.Players.LocalPlayer.Backpack:FindFirstChild("Horo-Horo")then 
                                                                    game.Players.LocalPlayer.Character.Humanoid:EquipTool(game.Players.LocalPlayer.Backpack:FindFirstChild("Horo-Horo"));
                                                                elseif game.Players.LocalPlayer.Character:FindFirstChild("Horo-Horo")then 
                                                                    if not game:GetService("Workspace").Ragdolls:FindFirstChild(game.Players.LocalPlayer.Name)then 
                                                                        repeat wait(1);
                                                                            if not game:GetService("Workspace").PlayerCharacters:FindFirstChild(game.Players.LocalPlayer.Name.."'s Main Body")then 
                                                                                game:GetService("VirtualInputManager"):SendKeyEvent(true,"T",false,game);
                                                                            end;
                                                                        until game:GetService("Workspace").PlayerCharacters:FindFirstChild(game.Players.LocalPlayer.Name.."'s Main Body")or not _G.Settings.Auto_Farm_Dungeon;
                                                                        wait(4);
                                                                    end;
                                                                end;
                                                            else ToTarget(CFrame.new(-908,131,-154));
                                                            end;
                                                        elseif game:GetService("Workspace").Islands:FindFirstChild("Mysterious Dungeon")then 
                                                            if game.Players.LocalPlayer:DistanceFromCharacter(Vector3.new(-1220,172,99))<=5 then 
                                                                if game.Players.LocalPlayer.Backpack:FindFirstChild("Horo-Horo")then 
                                                                    game.Players.LocalPlayer.Character.Humanoid:EquipTool(game.Players.LocalPlayer.Backpack:FindFirstChild("Horo-Horo"));
                                                                elseif game.Players.LocalPlayer.Character:FindFirstChild("Horo-Horo")then 
                                                                    if not game:GetService("Workspace").Ragdolls:FindFirstChild(game.Players.LocalPlayer.Name)then 
                                                                        repeat wait(1);
                                                                            if not game:GetService("Workspace").PlayerCharacters:FindFirstChild(game.Players.LocalPlayer.Name.."'s Main Body")then 
                                                                                game:GetService("VirtualInputManager"):SendKeyEvent(true,"T",false,game);
                                                                            end;
                                                                        until game:GetService("Workspace").PlayerCharacters:FindFirstChild(game.Players.LocalPlayer.Name.."'s Main Body")or not _G.Settings.Auto_Farm_Dungeon;
                                                                        wait(4);
                                                                    end;
                                                                end;
                                                            else ToTarget(CFrame.new(-1220,172,99));
                                                            end;
                                                        end;
                                                    end;
                                                else if game.Players.LocalPlayer.PlayerGui.Matchmake.TextLabel.Text~="GAME OVER"then 
                                                    ToTarget(c.HumanoidRootPart.CFrame);
                                                end;
                                            end;
                                        end);
                                    until not c or not c:FindFirstChild("Humanoid")or c.Humanoid.Health==0 or not _G.Settings.Auto_Farm_Dungeon;
                                end;
                            end;
                        else if game:GetService("Workspace").Islands:FindFirstChild("Tropical Island")then 
                            if game.Players.LocalPlayer:DistanceFromCharacter(Vector3.new(747,218,342))<=5 then 
                                if game.Players.LocalPlayer.Backpack:FindFirstChild("Horo-Horo")then 
                                    game.Players.LocalPlayer.Character.Humanoid:EquipTool(game.Players.LocalPlayer.Backpack:FindFirstChild("Horo-Horo"));
                                elseif game.Players.LocalPlayer.Character:FindFirstChild("Horo-Horo")then 
                                    if not game:GetService("Workspace").Ragdolls:FindFirstChild(game.Players.LocalPlayer.Name)then 
                                        repeat wait(1);
                                            if not game:GetService("Workspace").PlayerCharacters:FindFirstChild(game.Players.LocalPlayer.Name.."'s Main Body")then 
                                                game:GetService("VirtualInputManager"):SendKeyEvent(true,"T",false,game);
                                            end;
                                        until game:GetService("Workspace").PlayerCharacters:FindFirstChild(game.Players.LocalPlayer.Name.."'s Main Body")or not _G.Settings.Auto_Farm_Dungeon;
                                        wait(4);
                                    end;
                                end;
                            else ToTarget(CFrame.new(747,218,342));
                            end;
                        elseif game:GetService("Workspace").Islands:FindFirstChild("Sky Islands")then 
                            if game.Players.LocalPlayer:DistanceFromCharacter(Vector3.new(-908,131,-154))<=5 then 
                                if game.Players.LocalPlayer.Backpack:FindFirstChild("Horo-Horo")then 
                                    game.Players.LocalPlayer.Character.Humanoid:EquipTool(game.Players.LocalPlayer.Backpack:FindFirstChild("Horo-Horo"));
                                elseif game.Players.LocalPlayer.Character:FindFirstChild("Horo-Horo")then 
                                    if not game:GetService("Workspace").Ragdolls:FindFirstChild(game.Players.LocalPlayer.Name)then 
                                        repeat wait(1);
                                            if not game:GetService("Workspace").PlayerCharacters:FindFirstChild(game.Players.LocalPlayer.Name.."'s Main Body")then 
                                                game:GetService("VirtualInputManager"):SendKeyEvent(true,"T",false,game);
                                            end;
                                        until game:GetService("Workspace").PlayerCharacters:FindFirstChild(game.Players.LocalPlayer.Name.."'s Main Body")or not _G.Settings.Auto_Farm_Dungeon;
                                        wait(4);
                                    end;
                                end;
                            else ToTarget(CFrame.new(-908,131,-154));
                            end;
                        elseif game:GetService("Workspace").Islands:FindFirstChild("Mysterious Dungeon")then 
                            if game.Players.LocalPlayer:DistanceFromCharacter(Vector3.new(-1220,172,99))<=5 then 
                                if game.Players.LocalPlayer.Backpack:FindFirstChild("Horo-Horo")then 
                                    game.Players.LocalPlayer.Character.Humanoid:EquipTool(game.Players.LocalPlayer.Backpack:FindFirstChild("Horo-Horo"));
                                elseif game.Players.LocalPlayer.Character:FindFirstChild("Horo-Horo")then 
                                    if not game:GetService("Workspace").Ragdolls:FindFirstChild(game.Players.LocalPlayer.Name)then 
                                        repeat wait(1);
                                            if not game:GetService("Workspace").PlayerCharacters:FindFirstChild(game.Players.LocalPlayer.Name.."'s Main Body")then 
                                                game:GetService("VirtualInputManager"):SendKeyEvent(true,"T",false,game);
                                            end;
                                        until game:GetService("Workspace").PlayerCharacters:FindFirstChild(game.Players.LocalPlayer.Name.."'s Main Body")or not _G.Settings.Auto_Farm_Dungeon;
                                        wait(4);
                                    end;
                                end;
                            else ToTarget(CFrame.new(-1220,172,99));
                            end;
                        end;
                    end;
                end;
            end;
        end;
    end;
end);

k:AddToggle({Name="Auto Store Fruits",Value=_G.Settings.Auto_Store_Fruit,Locked=false,Callback=function(M)
    _G.Settings.Auto_Store_Fruit=M;
    B();
end});
task.spawn(function()
    repeat wait();
    until _G.Settings.Auto_Store_Fruit;
    while true do wait();
        if _G.Settings.Auto_Store_Fruit then 
            a=game:GetService("ReplicatedStorage")["Stats"..game.Players.LocalPlayer.Name].Inventory.Inventory.Value;
            for H,X in pairs(game:GetService("Players").LocalPlayer.Backpack:GetChildren())do 
                if X:IsA("Tool")and X:FindFirstChild("FruitEater")and not string.find(a,tostring(X.Name))then 
                    game.Players.LocalPlayer.Character.Humanoid:EquipTool(X);
                end;
            end;
            for D,p in pairs(game:GetService("Players").LocalPlayer.Character:GetChildren())do 
                if p:IsA("Tool")and p:FindFirstChild("FruitEater")and not string.find(a,tostring(p.Name))then game:GetService("ReplicatedStorage").Events.FruitStorage:InvokeServer(true);
                end;
            end;
        end;
    end;
end);

local f=j:CreateSection({Name="Moddified",Side='Left'});
local U=function(C,c)
    pcall(function()
        local D=require(game.ReplicatedStorage.Modules.SwordHandle.SwordInfo);
        local S;
        for V,J in pairs(game.Players.LocalPlayer.Backpack:GetChildren())do 
            if J:FindFirstChild("SwordEquip")then 
                S=J.Name;
            end;
        end;
        for l,X in pairs(game.Players.LocalPlayer.Character:GetChildren())do 
            if X:FindFirstChild("SwordEquip")then 
                S=X.Name;
            end;
        end;
        D[S][C]=c;
    end);
end;

f:AddToggle({Name="Long Range",Value=false,Locked=false,Callback=function(R)
    if R then 
        U("Range",Vector3.new(99,99,99));
    else U("Range",Vector3.new(10,10,10));
    end;
end});

f:AddToggle({Name="No Cooldown",Value=false,Locked=false,Callback=function(V)
    if V then 
        U("cooldown",0);
    else U("cooldown",0.425);
    end;
end});
local n=j:CreateSection({Name="Train Haki",Side='Left'});
n:AddToggle({Name="Auto Train Buso Haki",Value=_G.Settings.Auto_Train_Buso_Haki,Locked=false,Callback=function(i)
    _G.Settings.Auto_Train_Buso_Haki=i;
    B();
end});
n:AddToggle({Name="Finish Mini Game V2",Value=_G.Settings.Auto_Finish_Mini,Locked=false,Callback=function(D)
    _G.Settings.Auto_Finish_Mini=D;
    B();
end});
local r=j:CreateSection({Name="Settings",Side='Right'});
local Y={"Rifle"};
r:AddDropdown({Name="Select Combat / Weapons",Value=_G.Settings.Selected_Weapons,List=Y,Callback=function(K,I)
    _G.Settings.Selected_Weapons=K;
    B();
end});
r:AddToggle({Name="Safe Modes",Value=_G.Settings.Safe_Modes,Locked=false,Callback=function(J)
    _G.Settings.Safe_Modes=J;
    B();
end});
local e=tostring(game.Players.LocalPlayer.Name);
r:AddToggle({Name="Hide Name",Value=_G.Settings.Hide_Name,Locked=false,Callback=function(i)
    _G.Settings.Hide_Name=i;
    B();
    if not _G.Settings.Hide_Name then 
        pcall(function()
            game:GetService("CoreGui").PlayerList.PlayerListMaster.OffsetFrame.PlayerScrollList.SizeOffsetFrame.ScrollingFrameContainer.ScrollingFrameClippingFrame.ScollingFrame.OffsetUndoFrame["p_"..game.Players.LocalPlayer.UserId].ChildrenFrame.NameFrame.BGFrame.OverlayFrame.PlayerName.PlayerName.Text=e;end);end;end});
            local T=j:CreateSection({Name="Stats",Side='Right'});
            All_Stats={"Strength","Stamina","Defense"};
            for X,N in pairs(game:GetService("ReplicatedStorage")["Stats"..game.Players.LocalPlayer.Name].Stats:GetChildren())do 
                if N.Name:find("Mastery")then 
                    table.insert(All_Stats,tostring(N.Name));
                end;
            end;
            getgenv().Select_Stats2=_G.Settings.Select_Stats;
            local h=T:AddDropdown({Name="Select Stats",Multiple=true,List=All_Stats,Callback=function(J,K)
                _G.Settings.Select_Stats=J;
                B();
            end});
            pcall(function()
                h:Set(getgenv().Select_Stats2);
            end);
            T:AddToggle({Name="Auto Stats",Value=_G.Settings.Auto_Stats,Locked=false,Callback=function(C)
                _G.Settings.Auto_Stats=C;
                B();
            end});
            task.spawn(function()
                repeat wait();
                until _G.Settings.Auto_Stats;
                while true do wait(1);
                    if _G.Settings.Auto_Stats then 
                        for R,X in pairs(_G.Settings.Select_Stats)do 
                            if game:GetService("ReplicatedStorage")["Stats"..game.Players.LocalPlayer.Name].Stats.JailTime.Value==0 then 
                                if not game.Players.LocalPlayer.PlayerGui:FindFirstChild("DEATHGUI")then 
                                    if game:GetService("ReplicatedStorage")["Stats"..game.Players.LocalPlayer.Name].Stats.SkillPoints.Value~=0 then 
                                        local H={[1]=tostring(X),[3]=3};
                                        game:GetService("ReplicatedStorage").Events.stats:FireServer(unpack(H));
                                    end;
                                end;
                            end;
                        end;
                    end;
                end;
            end);
            local q=j:CreateSection({Name="LocalPlayer",Side='Right'});
            q:AddSlider({Name="WalkSpeed",Min=0,Max=100,Value=_G.Settings.WalkSpeed,Callback=function(p,K)
                _G.Settings.WalkSpeed=p;
                B();
                game.Players.LocalPlayer.Character.Humanoid.WalkSpeed=tonumber(_G.Settings.WalkSpeed);
            end});
            q:AddSlider({Name="JumpPower",Min=0,Max=500,Value=_G.Settings.JumpPower,Callback=function(D,R)
                _G.Settings.JumpPower=D;
                B();
                game.Players.LocalPlayer.Character.Humanoid.JumpPower=tonumber(_G.Settings.WalkSpeed);
            end});
            q:AddToggle({Name="No Crash Ship Damage",Value=_G.Settings.No_CrashShip_Damage,Locked=false,Callback=function(i)
                _G.Settings.No_CrashShip_Damage=i;
                B();
            end});
            q:AddToggle({Name="Walk On Water",Value=_G.Settings.Walk_On_Water,Locked=false,Callback=function(D)
                _G.Settings.Walk_On_Water=D;
                B();
            end});
            q:AddToggle({Name="Inf Dodge",Value=_G.Settings.Inf_Dodge,Locked=false,Callback=function(K)
                _G.Settings.Inf_Dodge=K;
                B();
            end});
            q:AddToggle({Name="Inf Geppo",Value=_G.Settings.Inf_Geppo,Locked=false,Callback=function(c)
                _G.Settings.Inf_Geppo=c;
                B();
            end});
            q:AddToggle({Name="No Fall Damage",Value=_G.Settings.No_Fall_Damage,Locked=false,Callback=function(J)
                _G.Settings.No_Fall_Damage=J;
                B();
            end});
            q:AddToggle({Name="No Drown",Value=_G.Settings.No_Drown,Locked=false,Callback=function(c)
                _G.Settings.No_Drown=c;
                B();
            end});
            local o=j:CreateSection({Name="Miscellaneous",Side='Right'});
            o:AddTextBox({Name="PS CODE",Value=_G.Settings.PS_Code,Placeholder="Enter PS Here.",Callback=function(R,l)
                _G.Settings.PS_Code=l;
                B();
            end});
            o:AddToggle({Name="Enabled",Value=_G.Settings.PS_Rejoin,Locked=false,Callback=function(c)
                _G.Settings.PS_Rejoin=c;
                B();
            end});
            task.spawn(function()
                repeat wait();
                until _G.Settings.PS_Code~=nil and _G.Settings.PS_Rejoin==true;
                while true do wait();
                    if _G.Settings.PS_Code~=nil and _G.Settings.PS_Rejoin==true then 
                        pcall(function()
                            game:GetService("ReplicatedStorage").Events.reserved:InvokeServer(tostring(_G.Settings.PS_Code));
                        end);
                    end;
                end;
            end);
            o:AddLabel({Text="Miscellaneous"});
            o:AddToggle({Name="Full Bright",Value=_G.Settings.Full_Bright,Locked=false,Callback=function(C)
                _G.Settings.Full_Bright=C;
                B();
                if getgenv().brightLoop then 
                    getgenv().brightLoop:Disconnect();
                end;
                local function V()
                    if not _G.Settings.Full_Bright then 
                        getgenv().brightLoop:Disconnect();
                    end;
                    game:GetService("Lighting").Brightness=2;
                    game:GetService("Lighting").ClockTime=14;
                    game:GetService("Lighting").FogEnd=100000;
                    game:GetService("Lighting").GlobalShadows=false;
                    game:GetService("Lighting").OutdoorAmbient=Color3.fromRGB(128,128,128);
                end;
                getgenv().brightLoop=game:GetService("RunService").RenderStepped:Connect(V);
                local p,S,D,W,I=game:GetService("Lighting").Brightness,game:GetService("Lighting").ClockTime,game:GetService("Lighting").FogEnd,game:GetService("Lighting").GlobalShadows,game:GetService("Lighting").OutdoorAmbient;
                if t then 
                    game:GetService("Lighting").Brightness=2;
                    game:GetService("Lighting").ClockTime=14;
                    game:GetService("Lighting").FogEnd=100000;
                    game:GetService("Lighting").GlobalShadows=false;
                    game:GetService("Lighting").OutdoorAmbient=Color3.fromRGB(128,128,128);
                else game:GetService("Lighting").Brightness=p;
                    game:GetService("Lighting").ClockTime=S;
                    game:GetService("Lighting").FogEnd=D;
                    game:GetService("Lighting").GlobalShadows=W;
                    game:GetService("Lighting").OutdoorAmbient=I;
                end;
            end});
            o:AddToggle({Name="No Fog",Value=_G.Settings.No_Fog,Locked=false,Callback=function(K)
                _G.Settings.No_Fog=K;
                B();
                if _G.Settings.No_Fog then 
                    game:GetService("Lighting").FogEnd=100000;
                    for X,J in pairs(game:GetService("Lighting"):GetDescendants())do 
                        if J:IsA("Atmosphere")then J.Parent=game:GetService("TestService");
                        end;
                    end;
                else for I,d in pairs(game:GetService("TestService"):GetDescendants())do 
                    if d:IsA("Atmosphere")then 
                        d.Parent=game:GetService("Lighting");
                    end;
                end;
                game:GetService("Lighting").FogEnd=1024;
            end;
        end});
        o:AddToggle({Name="Auto Kick",Value=_G.Settings.Auto_Kick,Locked=false,Callback=function(u)
            _G.Settings.Auto_Kick=u;
            B();
        end});
        game:GetService("Players").PlayerAdded:Connect(function(w)
            if _G.Settings.Auto_Kick then 
                if not w:IsFriendsWith(game.Players.LocalPlayer.UserId)then 
                    game.Players.LocalPlayer:Kick(w.Name.." joined the game!");
                end;
            end;
        end);
    end;
    task.spawn(function()
        while true do wait();
            repeat wait();
            until _G.Settings.Auto_Farm_Level or _G.Settings.Auto_Farm_Ship or _G.Settings.Auto_Farm_Dungeon or _G.Settings.Auto_Train_Buso;
            if _G.Settings.Auto_Farm_Level or _G.Settings.Auto_Farm_Ship or _G.Settings.Auto_Farm_Dungeon or _G.Settings.Auto_Train_Buso then 
                if game:GetService("ReplicatedStorage")["Stats"..game.Players.LocalPlayer.Name].Stats.BusoMastery.Value~=0 and game:GetService("ReplicatedStorage")["Stats"..game.Players.LocalPlayer.Name].BusoBar.Value~=0 then 
                    if IsBuso()==false then 
                        game:GetService("VirtualInputManager"):SendKeyEvent(true,"J",false,game);
                    end;
                end;
            end;
        end;
    end);
    loadstring(game:HttpGet("https://androssy.net/TrashXenon/GPO_Noclip.lua",true))();
    task.spawn(function()
        repeat wait();
        until _G.Settings.Auto_Farm_Level or _G.Settings.Auto_Farm_Ship or _G.Teleport or _G.Settings.Auto_Farm_Dungeon;
        while true do wait();
            if _G.Settings.Auto_Farm_Level or _G.Settings.Auto_Farm_Ship or _G.Teleport or _G.Settings.Auto_Farm_Dungeon then 
                if game:GetService("ReplicatedStorage")["Stats"..game.Players.LocalPlayer.Name].Stats.JailTime.Value==0 then 
                    if not game.Players.LocalPlayer.PlayerGui:FindFirstChild("DEATHGUI")then 
                        if not game.Players.LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BV")then 
                            pcall(function()
                                game.Players.LocalPlayer.Character:FindFirstChildOfClass('Humanoid').Sit=false;
                            end);
                            local n=Instance.new("BodyVelocity");
                            n.Parent=game.Players.LocalPlayer.Character.HumanoidRootPart;
                            n.Name="BV";
                            n.MaxForce=Vector3.new(100000,100000,100000);
                            n.Velocity=Vector3.new(0,0,0);
                        end;
                    end;
                end;
            else if game.Players.LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BV")then 
                game.Players.LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BV"):Remove();
            end;
        end;
    end;
end);
task.spawn(function()
    while true do wait(5);
        pcall(function()
            for n,u in pairs(game.Players.LocalPlayer.PlayerGui.HUD.Buso.BBar:GetChildren())do 
                if u.Name=="a"then
                    u:Remove();
                end;
                end;
            end);
        end;
    end);
    task.spawn(function()
        if _G.Settings.Hide_Name then 
            pcall(function()
                game:GetService("CoreGui").PlayerList.PlayerListMaster.OffsetFrame.PlayerScrollList.SizeOffsetFrame.ScrollingFrameContainer.ScrollingFrameClippingFrame.ScollingFrame.OffsetUndoFrame["p_"..game.Players.LocalPlayer.UserId].ChildrenFrame.NameFrame.BGFrame.OverlayFrame.PlayerName.PlayerName.Text="PROTECTED BY XENON";
            end);
        end;
    end);
    task.spawn(function()
        while true do wait();
            if _G.Settings.Hide_Name then 
                pcall(function()
                    game:GetService("CoreGui").PlayerList.PlayerListMaster.OffsetFrame.PlayerScrollList.SizeOffsetFrame.ScrollingFrameContainer.ScrollingFrameClippingFrame.ScollingFrame.OffsetUndoFrame["p_"..game.Players.LocalPlayer.UserId].ChildrenFrame.NameFrame.BGFrame.OverlayFrame.PlayerName.PlayerName.Text="PROTECTED BY XENON";
                end);
            end;
        end;
    end);
    local Z=getconnections or get_signal_cons;
    if Z then warn("Anti AFK Activated");
        for D,p in pairs(Z(game.Players.LocalPlayer.Idled))do 
            if p["Disable"]then 
                p["Disable"](p);
            elseif p["Disconnect"]then p["Disconnect"](p);
            end;
        end;
        for J,u in next,Z(game.Players.LocalPlayer.Idled)do 
            u:Disable();
        end;
    else game.Players.LocalPlayer:Kick("Missing getconnections() functions executer not supported");
    end;
    game.Players.PlayerAdded:Connect(function(Y)
        if Y:IsInGroup(3229308)then 
            game.Players.LocalPlayer:Kick("Mods Joined :"..tostring(Y.Name));
        end;
    end);
end;
A();
