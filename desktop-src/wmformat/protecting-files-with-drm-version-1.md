---
title: 使用 DRM 第1版保護檔案
description: 使用 DRM 第1版保護檔案
ms.assetid: 91de1c20-e926-4ff6-b0cd-e90fc9cbaad2
keywords:
- Windows Media Format SDK，建立受保護的檔案
- Windows Media Format SDK，受保護的檔案
- Advanced Systems Format (ASF) ，建立受保護的檔案
- ASF (Advanced Systems Format) ，建立受保護的檔案
- Advanced Systems Format (ASF) 、受保護的檔案
- ASF (Advanced 系統格式) 、受保護的檔案
- Advanced Systems Format (ASF) ，WMStubDRM .lib
- ASF (Advanced Systems Format) ，WMStubDRM .lib
- WMStubDRM .lib，建立受保護的檔案
- WMStubDRM .lib，受保護的檔案
- 數位版權管理 (DRM) ，WMStubDRM .lib
- DRM (數位版權管理) ，WMStubDRM .lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3e4d1ae9c0d3835c20f75b4e61c262a85a26f4
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "104314517"
---
# <a name="protecting-files-with-drm-version-1"></a>使用 DRM 第1版保護檔案

套用這種類型的保護時，會產生僅在提出授權要求的電腦上有效的 DRM 第1版授權。 因為未設定任何金鑰或金鑰種子，所以無法使用這項技術來產生受保護內容的可移植授權。 不過，使用 Windows Media 格式 SDK 7.1 或更新版本時，授權可在 Microsoft 授權遷移服務復原。

若要使用 DRM 第1版保護 ASF 檔案，請執行下列步驟：

1.  將 WMStubDRM .lib 檔案連結至您的專案，如有必要，請將 wmvcore 取消連結。
2.  呼叫 [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) 函數來建立寫入器。 第一個引數是保留的，而且必須設定為 **Null**。
3.  藉由呼叫 [**IWMWriter：： SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) 或 [**IWMWriter：： SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid)，設定要使用之寫入器的設定檔。 設定任何 DRM 屬性之前，您必須先在寫入器中設定設定檔。 只有使用 Windows Media 音訊或 Windows Media 視訊編解碼器的設定檔才支援 DRM。
4.  使用 [**IWMHeaderInfo：： SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) 方法，設定下列 DRM 屬性。 [ **使用 \_ drm** ] 屬性會指示 DRM 元件使用 drm 第1版來保護內容。 [ **DRM \_ 旗標** ] 屬性會指定要為內容建立的本機授權包含的許可權。 **DRM \_ 層級** 值也會儲存在授權中，它會指定存取內容所需的最低層級。 150是 DRM 第1版內容的建議等級。

    | 屬性      | 值                                                                                       |
    |----------------|---------------------------------------------------------------------------------------------|
    | **使用 \_ DRM**   | **TRUE**                                                                                    |
    | **DRM \_ 旗標** | WMT \_ RIGHT \_ 播放 \| WMT 以 \_ 右鍵 \_ 複製 \_ 至 \_ 非 \_ SDMI \_ 裝置 \| WMT \_ 從右 \_ 複製 \_ 到 \_ CD |
    | **DRM \_ 層級** | 150                                                                                         |

    

     

下列範例程式碼示範如何針對 DRM 第1版建立啟用 DRM 的寫入器，並設定 DRM 屬性。 為了清楚起見，已省略錯誤檢查。


```C++
BOOL  fUseDRM    = TRUE;
// These are the rights we will apply to the file. See WMT_RIGHTS for
// the full set of possible rights.

DWORD dwDRMFlags = WMT_RIGHT_PLAYBACK | 
                   WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE | 
                   WMT_RIGHT_COPY_TO_CD;

// Set the minimum required DRM level low enough
// to allow older players to access the content.
DWORD dwDRMLevel = 150;

IWMDRMWriter*  pWMDRMWriter  = NULL;
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a writer object.
hr = WMCreateWriter( NULL, &pWMDRMWriter);

// Obtain the IWMHeaderInfo interface.
hr = pWMDRMWriter -> QueryInterface(IID_IWMHeaderInfo, 
                                   (void**) &pWMHeaderInfo);

// Tell the SDK runtime to protect the file using DRM version 1.
hr= pWMHeaderInfo-> SetAttribute(0,
                                 g_wszWMUse_DRM,
                                 WMT_TYPE_BOOL,
                                 (BYTE*)&fUseDRM,
                                 sizeof(BOOL));

// Specify the rights that will be stored in the local license that is
// created automatically for the content.
hr= pWMHeaderInfo->SetAttribute( 0,
                                 g_wszWMDRM_Flags, 
                                 WMT_TYPE_DWORD,
                                 (BYTE *)&dwDRMFlags,
                                 sizeof(DWORD) );

// Set the DRM_Level attribute in the file's DRM header.
hr= pWMHeaderInfo->SetAttribute( 0,
                                 g_wszWMDRM_Level, 
                                 WMT_TYPE_DWORD,
                                 (BYTE *)&dwDRMLevel,
                                 sizeof(DWORD) );
```



 

 




