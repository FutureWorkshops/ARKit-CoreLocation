source 'https://github.com/CocoaPods/Specs.git'
platform :ios, '11.0'
use_frameworks!

target 'ARKit+CoreLocation' do
	pod 'CocoaLumberjack/Swift', :git => 'https://github.com/CocoaLumberjack/CocoaLumberjack', :branch => 'master'
end

post_install do |installer|
    installer.pods_project.targets.each do |target|
        if target.name == 'CocoaLumberjack'
            target.build_configurations.each do |config|
                config.build_settings['SWIFT_VERSION'] = '3.2'
            end
        end
    end
end
