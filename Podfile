platform :ios, '15.0'
use_frameworks!
inhibit_all_warnings!

def testing_pods
  pod 'SwiftFormat/CLI'
  pod 'OHHTTPStubs/Swift', :configurations => ['Debug Development', 'Debug Staging', 'Debug Production']
end

target 'KnowledgeCards' do
  # UI
  pod 'Kingfisher'

  # Backend
  pod 'Alamofire'

  # Storage
  pod 'KeychainAccess'

  # Tools
  pod 'Firebase/Crashlytics'
  pod 'R.swift'
  pod 'Factory'

  # Development
  pod 'SwiftLint'
  pod 'Wormholy', :configurations => ['Debug Development', 'Debug Staging', 'Debug Production']
  pod 'xcbeautify'

  target 'KnowledgeCardsTests' do
    inherit! :search_paths
    testing_pods
  end

end

def data_dependencies
  pod 'Alamofire'
end

target 'Data' do
  data_dependencies

  target 'DataTests' do
    data_dependencies
    testing_pods
  end
end

target 'Domain' do
  target 'DomainTests' do
    testing_pods
  end
end

post_install do |installer|
  installer.pods_project.targets.each do |target|
  end
end
