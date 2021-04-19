---
description: 本主題適用于 Windows Vista 和更新版本。
ms.assetid: 4d88806a-68a6-4394-a704-c7a47a0fdc70
title: 與 Windows 影像中心和 Windows 檔案總管整合
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b2ab2bb725b151a069f53a94a8fb2e31766132d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994396"
---
# <a name="integration-with-windows-photo-gallery-and-windows-explorer"></a>與 Windows 影像中心和 Windows 檔案總管整合

本主題適用于 Windows Vista 和更新版本。 它包含下列區段：

-   [簡介](#introduction)
-   [與 Windows 屬性儲存區整合](#integration-with-the-windows-property-store)
-   [與 Windows 影像中心整合](#integration-with-the-windows-photo-gallery)
-   [與 Windows 縮圖快取整合](#integration-with-the-windows-thumbnail-cache)
-   [相關主題](#related-topics)

## <a name="introduction"></a>簡介

若要讓 Windows 影像中心和 Windows 檔案總管顯示縮圖和搜尋和更新標準影像中繼資料，編解碼器必須具有與其相關聯的 [IThumbnailProvider](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) 和 [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) 介面的執行。 IThumbnailProvider 介面是用來抓取縮圖並填入縮圖快取，而 IPropertyStore 介面是用來搜尋和更新與檔案相關聯的中繼資料。 在 Windows Vista 中，所有檔案類型都有縮圖和中繼資料，但不同的檔案類型需要這些介面的不同執行，以抓取或產生它們的縮圖和中繼資料。 系統會提供這些介面的預設執行。 IThumbnailProvider 的預設執行可用於任何 Windows 影像處理元件 (WIC) 啟用的映射格式。 IPropertyStore 的預設執行可搭配任何已啟用 WIC 的映射格式使用，此格式以標記的影像檔案格式為基礎， (TIFF) 或 JPEG 容器。 若要將映射格式與這兩個介面的預設執行建立關聯，您必須只新增一些登錄專案。

下列專案指出 Windows 影像中心，並 Windows 檔案總管副檔名 () 及其相關聯的 MIME 類型與影像格式相關聯。

下列專案表示使用內容類型 (也稱為 mime 類型的 Windows 和應用程式) 具有指定副檔名 ( 的檔案。 ext) 是影像格式。 檔案類型擁有者必須選擇可 `<image sub type value>` 唯一識別檔案格式的，且此內容類型值必須向 IANA 註冊。

```
HKEY_CLASSES_ROOT
   {.ext}
      ContentType = image/<image sub type>
```

下列專案 [指出使用 system.string 的 windows](../properties/props-system-kind.md) 、windows 搜尋和應用程式（副檔名)  (）應該視為一張圖片。 具體而言，它會指出副檔名的 System.object 屬性應該設定為 Picture。

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  KindMap
                     {.ext} = Picture
```

## <a name="integration-with-the-windows-property-store"></a>與 Windows 屬性儲存區整合

有時候，相同的中繼資料屬性會在不同的中繼資料架構中公開，通常會有不同的屬性名稱。 當更新其中一個屬性，但其他屬性不是時，檔案內的中繼資料可能會不同步。Photo 屬性處理常式會提供映射的預設 **IPropertyStore** 執行，並由應用程式以及 windows 影像中心和 Windows 檔案總管確保影像中的所有中繼資料都保持同步，而且應用程式所顯示的屬性與 Windows 影像中心和 Windows 檔案總管所顯示的屬性一致。 當相片屬性處理常式更新中繼資料時，會確定這些屬性會在檔案中的所有通用元資料格式中一致更新。

Photo 屬性處理常式必須瞭解容器格式，以及如何找出其內的各種屬性。 一般而言，相片屬性處理常式不可能知道如何以專屬的容器格式來配置各種不同的中繼資料區塊。 但是，如果您的容器格式中繼資料的配置方式與 TIFF 容器格式或 JPEG 容器格式的中繼資料相同，則相片屬性處理常式也可以利用該知識，以一致的方式更新您的容器格式的中繼資料。

您可以藉由建立下列登錄專案來註冊此關聯。 此專案會通知相片屬性處理常式，此 GUID 所識別的容器格式可理解與具有 GUID 163bcc30-e2e9-4f0b-961d-a3e9fdb788a3 的容器格式相同的中繼資料查詢語言路徑。  (163bcc30-e2e9-4f0b-961d-a3e9fdb788a3 是 TIFF 容器格式的 GUID。 ) 

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PhotoPropertyHandler
                  ContainerAssociations
                     {Container Format GUID} = {163bcc30-e2e9-4f0b-961d-a3e9fdb788a3}
```

下列專案會將相片屬性處理常式的預設實 **IPropertyStore** 與副檔名為 "ext" 的檔案產生關聯。 第一個 GUID 是 **IPropertyStore** 介面的 IID，而第二個則是相片屬性處理常式之執行的 guid。

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PhotoPropertyHandler
                  {.ext}
                     (Default) = {a38b883c-1682-497e-97b0-0a3a9e801682}
```

使用與 TIFF 或 JPEG 容器格式不相容之專屬格式的編解碼器必須撰寫自己的 **IPropertyStore** 執行。

## <a name="integration-with-the-windows-photo-gallery"></a>與 Windows 影像中心整合

Windows 影像中心是以 WIC 為基礎建立的，而且可以顯示已安裝任何已啟用 WIC 之編解碼器的映射格式。 若要通知系統您的映射格式可在 Windows 影像中心中開啟，您必須建立下列登錄專案來建立檔案關聯。

```
HKEY_CLASSES_ROOT
   {.ext}
      (Default) = {ProgID} for example, jpegfile)
      OpenWithProgids
         {ProgID}
      OpenWithList
         PhotoViewer.dll
      ShellEx
         ContextMenuHandlers
            ShellImagePreview
               (Default) = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
   SystemFileAssociations
      {.ext}
         OpenWithList
            PhotoViewer.dll
         ShellEx
            ContextMenuHandlers
               ShellImagePreview
                  (Default) = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
   {Image Format ProgID}
      (Default) = Name of Image Format
      DefaultIcon
         (Default) = Path to icon for type, icon index
      shell
         open
            MuiVerb = @%PROGRAMFILES%\Windows Photo Gallery\photoviewer.dll,-3043
            command
               (Default) = %SystemRoot%\System32\rundll32.exe "%ProgramFiles%\Windows Photo Gallery\PhotoViewer.dll", ImageView_Fullscreen %1
            DropTarget
               Clsid = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
         printo
            command
               (Default) = %SystemRoot%\System32\rundll32.exe "%SystemRoot%\System32\shimgvw.dll", ImageView_PrintTo /pt "%1" "%2" "%3" "%4"
```

ProgID 通常是附加在 "file" 這個字的副檔名。  (例如，如果副檔名為 .txt，則 ProgID 通常會是 "txtfile"。 ) 

您可能需要建立其他標準登錄專案來支援檔案關聯;不過，因為 the'y 不是 WIC 專屬的，所以它們已超出本主題的範圍。

## <a name="integration-with-the-windows-thumbnail-cache"></a>與 Windows 縮圖快取整合

下列兩個專案表示標準 WIC 縮圖提供者實作為此副檔名的檔案，可以用來取得縮圖。 第一個 GUID 是 [IThumbnailProvider](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) 介面的 IID，而第二個 guid 是此介面標準系統實作為的 guid。  (HLCR 下的所有專案 \\ \\ 都會在 \\ HKCR \\ SystemFileAssociations \\ . ext ShellEx 下重複 \\ 。 \\ ) 

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      {.ext}
         ShellEx
            {e357fccd-a995-4576-b01f-234630154e96}
               (Default) = {C7657C4A-9F68-40fa-A4DF-96BC08EB3551}
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[編碼器特定的登錄專案](-wic-decoderregentries.md)
</dt> <dt>

[編解碼器安裝和註冊](-wic-codecinstallandreg.md)
</dt> <dt>

[如何撰寫 WIC-Enabled 編解碼器](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows 影像處理元件總覽](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
