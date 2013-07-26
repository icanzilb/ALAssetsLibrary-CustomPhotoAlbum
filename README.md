ALAssetsLibrary-CustomPhotoAlbum
================================

# Description

A nice ALAssetsLibrary category for saving images into custom photo album by @MarinTodorov. I added new feature writeImageDataToSavedPhotosAlbumVural, You can save image from NSData and save photo metadata. @vuraltuna

## Usage

    //           |image|: the target image to be saved
    //       |albumName|: custom album name
    // |completionBlock|: block to be executed when succeed to write the image data
    //                    to the assets library (camera roll)
    //    |failureBlock|: block to be executed when failed to add the asset to the
    //                    custom photo album
    - (void)saveImage:(UIImage *)image
              toAlbum:(NSString *)albumName
      completionBlock:(ALAssetsLibraryWriteImageCompletionBlock)completionBlock
         failureBlock:(ALAssetsLibraryAccessFailureBlock)failureBlock;
         
         
##Using writeImageDataToSavedPhotosAlbumVural         
     
     //      |imageData|: the target image to be saved (NSData)
    //       |albumName|: custom album name (NSString)
    //		   |metadata|: Photo metadata (NSDictionary)
    // |completionBlock|: block to be executed when succeed to write the image data
    //                    to the assets library (camera roll)
    //    |failureBlock|: block to be executed when failed to add the asset to the
    //                    custom photo album
        
     - (void)writeImageDataToSavedPhotosAlbumVural:(NSData *)imageData
        metadata:(NSDictionary *)metadata
        toAlbum:(NSString *)albumName
        completionBlock:(ALAssetsLibraryWriteImageCompletionBlock)completionBlock
        failureBlock:(ALAssetsLibraryAccessFailureBlock)failureBlock;    

##And for video:

    //        |videoUrl|: the target video to be saved
    //       |albumName|: custom album name
    // |completionBlock|: block to be executed when succeed to write the image data
    //                    to the assets library (camera roll)
    //    |failureBlock|: block to be executed when failed to add the asset to the
    //                    custom photo album
    - (void)saveVideo:(NSURL *)videoUrl
              toAlbum:(NSString *)albumName
      completionBlock:(ALAssetsLibraryWriteImageCompletionBlock)completionBlock
         failureBlock:(ALAssetsLibraryAccessFailureBlock)failureBlock;

# Dependence

  1. AssetsLibrary.framework
  2. MobileCoreServices.framework


# REFERENCE:

- [ALAssetsLibrary Class Reference][1]  
- [iOS5: Saving photos in custom photo album][2]

[1]: http://developer.apple.com/library/ios/#documentation/AssetsLibrary/Reference/ALAssetsLibrary_Class/Reference/Reference.html#//apple_ref/occ/instm/ALAssetsLibrary/addAssetsGroupAlbumWithName:resultBlock:failureBlock:
[2]: http://www.touch-code-magazine.com/ios5-saving-photos-in-custom-photo-album-category-for-download/
