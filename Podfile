# Uncomment this line to define a global platform for your project
# platform :ios, "7.0"

source 'https://github.com/CocoaPods/Specs.git'

post_install do |installer_representation|
  installer_representation.pods_project.targets.each do |target|
    puts "=== #{target.name}"
    if target.name == "AFNetworking"
      puts "Setting AFNetworking Macro AF_APP_EXTENSIONS so that it doesn't use UIApplication in extension."
      target.build_configurations.each do |config|
        puts "Setting AF_APP_EXTENSIONS macro in config: #{config}"
        config.build_settings['GCC_PREPROCESSOR_DEFINITIONS'] ||= ['$(inherited)', 'AF_APP_EXTENSIONS=1']
      end
    end
  end
end

#post_install do |installer_representation|
#  installer_representation.project.targets.each do |target|
#    if target.name == "ReactiveHackerNews"
#      target.build_configurations.each do |config|
#        config.build_settings['GCC_PREPROCESSOR_DEFINITIONS'] ||= ['$(inherited)', 'AF_APP_EXTENSIONS=1']
#      end
#    end
#  end
#end



target "ReactiveHackerNews" do
	pod 'pop'
	pod 'PureLayout'
	pod 'NSString-HTML'
	pod 'ZLSwipeableView'
	pod 'SVProgressHUD'
	pod 'NJKWebViewProgress'
	pod 'ReactiveCocoa', '~> 2.4.4'
	pod 'TUSafariActivity', '~> 1.0'
	pod 'AFNetworking', '~> 2.6.0'
	pod 'AFNetworkActivityLogger', '~> 2.0.3'
	pod 'AFNetworking2-RACExtensions', '~> 0.0'
end

target "ReactiveHackerNewsTests" do
	pod 'OCMock'
end

target 'HackerNewsToday' do
	pod 'ReactiveCocoa', '~> 2.4.4'
	pod 'AFNetworking', '~> 2.6.0'
	pod 'AFNetworkActivityLogger', '~> 2.0.3'
	pod 'AFNetworking2-RACExtensions', '~> 0.0'
end

target 'ReactiveHackerNews WatchKit Extension' do
	pod 'ReactiveCocoa', '~> 2.4.4'
	pod 'AFNetworking', '~> 2.6.0'
	pod 'AFNetworkActivityLogger', '~> 2.0.3'
	pod 'AFNetworking2-RACExtensions', '~> 0.0'
end

