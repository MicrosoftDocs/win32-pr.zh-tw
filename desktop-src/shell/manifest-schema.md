---
description: 這些元素組成 Web 發行和線上列印訂購嚮導的傳送資訊清單中所使用的 XML 架構。
title: 傳送資訊清單架構
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 488b6fc9-ff85-4860-9cd5-61d5de7e15e8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d0b57f1eb81169674c6c8d36e66c8a3cd21cf0e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991694"
---
# <a name="transfer-manifest-schema"></a>傳送資訊清單架構

這些元素組成 Web 發行和線上列印訂購嚮導的傳送資訊清單中所使用的 XML 架構。

下列是針對傳送資訊清單所定義的元素。

-   [cancelledpage](#syntax)
    -   [語法](#syntax)
    -   [屬性](#attributes)
    -   [項目資訊](#element-information)
-   [failurepage](#syntax)
    -   [語法](#syntax)
    -   [屬性](#attributes)
    -   [項目資訊](#element-information)
-   [喜歡](#syntax)
    -   [語法](#syntax)
    -   [屬性](#attributes)
    -   [項目資訊](#element-information)
-   [file](#syntax)
    -   [語法](#syntax)
    -   [屬性](#attributes)
    -   [項目資訊](#element-information)
-   [filelist](#syntax)
    -   [語法](#syntax)
    -   [屬性](#attributes)
    -   [項目資訊](#element-information)
-   [資料夾](#syntax)
    -   [語法](#syntax)
    -   [屬性](#attributes)
    -   [項目資訊](#element-information)
-   [folderlist](#syntax)
    -   [語法](#syntax)
    -   [屬性](#attributes)
    -   [項目資訊](#element-information)
-   [formdata](#syntax)
    -   [語法](#syntax)
    -   [屬性](#attributes)
    -   [項目資訊](#element-information)
-   [htmlui](#syntax)
    -   [語法](#syntax)
    -   [屬性](#attributes)
    -   [項目資訊](#element-information)
-   [imageproperty](#syntax)
    -   [語法](#syntax)
    -   [屬性](#attributes)
    -   [項目資訊](#element-information)
-   [元](#syntax)
    -   [語法](#syntax)
    -   [屬性](#attributes)
    -   [項目資訊](#element-information)
-   [netplace](#syntax)
    -   [語法](#syntax)
    -   [屬性](#attributes)
    -   [項目資訊](#element-information)
-   [發佈](#syntax)
    -   [語法](#syntax)
    -   [屬性](#attributes)
    -   [項目資訊](#element-information)
-   [調整](#syntax)
    -   [語法](#syntax)
    -   [屬性](#attributes)
    -   [項目資訊](#element-information)
-   [successpage](#syntax)
    -   [語法](#syntax)
    -   [屬性](#attributes)
    -   [項目資訊](#element-information)
-   [目標](#syntax)
    -   [語法](#syntax)
    -   [屬性](#attributes)
    -   [項目資訊](#element-information)
-   [transfermanifest](#syntax)
    -   [語法](#syntax)
    -   [屬性](#attributes)
    -   [項目資訊](#element-information)
-   [uploadinfo](#syntax)
    -   [語法](#syntax)
    -   [屬性](#attributes)
    -   [項目資訊](#element-information)

## <a name="cancelledpage"></a>cancelledpage

指定當使用者按一下 [ **取消** ] 按鈕時，在關閉嚮導之前顯示的伺服器端 HTML 網頁。

### <a name="syntax"></a>Syntax


```
<cancelledpage
    href = "string"
>
<!-- child elements -->
</cancelledpage>                  
                    
```



### <a name="attributes"></a>屬性



| 屬性 | 描述                                                                                           |
|-----------|-------------------------------------------------------------------------------------------------------|
| href      | 必要。 當使用者按一下 [ **取消** ] 按鈕時要顯示之伺服器端 HTML 頁面的 URL。 |



 

### <a name="element-information"></a>項目資訊



| Parent 項目        | 子元素 |
|-----------------------|----------------|
| [uploadinfo](#syntax) | 無           |



 

## <a name="failurepage"></a>failurepage

指定當上傳不成功時，要顯示的伺服器端 HTML 網頁。

### <a name="syntax"></a>Syntax


```
<failurepage
    href = "string"
>
<!-- child elements -->
</failurepage>                    
                    
```



### <a name="attributes"></a>屬性



| 屬性 | 描述                                                                                |
|-----------|--------------------------------------------------------------------------------------------|
| href      | 必要。 當上傳不成功時，要顯示之伺服器端 HTML 頁面的 URL。 |



 

### <a name="element-information"></a>項目資訊



| Parent 項目        | 子元素         |
|-----------------------|------------------------|
| [uploadinfo](#syntax) | 無。 允許文字。 |



 

## <a name="favorite"></a>我的最愛

指示嚮導在指定 URL 的 [我的最愛 **] 功能表中** 建立最愛的網站專案。 如果未指定這個元素，則會在其位置使用 [htmlui](#syntax) 元素。

### <a name="syntax"></a>Syntax


```
<favorite
    comment = "string"
    href = "string"
    name = "string"
>
<!-- child elements -->
</favorite>                   
                    
```



### <a name="attributes"></a>屬性



| 屬性 | 描述                                                            |
|-----------|------------------------------------------------------------------------|
| comment   | 必要。 與 [我的最愛 **]** 專案相關聯的批註。         |
| href      | 必要。 [我的最愛 **]** 專案的 URL。                          |
| NAME      | 必要。 出現在 [我的最愛 **]** 功能表中的 URL 名稱。 |



 

### <a name="element-information"></a>項目資訊



| Parent 項目        | 子元素         |
|-----------------------|------------------------|
| [uploadinfo](#syntax) | 無。 允許文字。 |



 

## <a name="file"></a>file

描述要複製的單一檔案。 單一[filelist](#syntax)節點底下可能[包含多個](#syntax)檔案元素。

### <a name="syntax"></a>Syntax


```
<file
    contenttype = "string"
    destination = "string"
    extension = "string"
    id = "string"
    size = "string"
    source = "string"
>
<!-- child elements -->
</file>                   
                    
```



### <a name="attributes"></a>屬性



| 屬性   | 描述                                                                                                                                                                  |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| contenttype | 選擇性。 檔案的 MIME 類型。                                                                                                                                         |
| 目的地 | 必要。 檔案上傳之後的建議路徑。 此路徑相對於上傳網站的目的地 URL。 上傳網站可以視需要修改此值。 |
| 擴充功能   | 選擇性。 檔案名的副檔名。                                                                                                                               |
| id          | 必要。 檔案的數值索引。                                                                                                                                   |
| {1}size{2}        | 選擇性。 檔案的大小（以位元組為單位）。                                                                                                                                    |
| source      | 必要。 檔案的完整檔案系統路徑。                                                                                                                            |



 

### <a name="element-information"></a>項目資訊



| Parent 項目      | 子元素                                          |
|---------------------|---------------------------------------------------------|
| [filelist](#syntax) | [中繼資料](#syntax)、 [貼](#syntax)文、重 [設大小](#syntax) |



 

## <a name="filelist"></a>filelist

描述要複製之檔案的元素容器。 單一[transfermanifest](#syntax)節點底下可能包含多個[filelist](#syntax)元素。

### <a name="syntax"></a>Syntax


```
<filelist
    usesfolders = "1"
>
<!-- child elements -->
</filelist>                   
                    
```



### <a name="attributes"></a>屬性



| 屬性   | 描述      |
|-------------|------------------|
| usesfolders | 未實作。 |



 

### <a name="element-information"></a>項目資訊



| Parent 項目              | 子元素  |
|-----------------------------|-----------------|
| [transfermanifest](#syntax) | [file](#syntax) |



 

## <a name="folder"></a>folder

描述儲存檔案的資料夾。 單一[folderlist](#syntax)節點底下可能包含多個[資料夾](#syntax)元素。

### <a name="syntax"></a>Syntax


```
<folder
    destination = "string"
>
<!-- child elements -->
</folder>                 
                    
```



### <a name="attributes"></a>屬性



| 屬性   | 描述                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 目的地 | 必要。 資料夾上傳之後的建議路徑。 此路徑相對於上傳網站的目的地 URL。 上傳網站可以視需要修改此值。 |



 

### <a name="element-information"></a>項目資訊



| Parent 項目        | 子元素 |
|-----------------------|----------------|
| [folderlist](#syntax) | 無           |



 

## <a name="folderlist"></a>folderlist

描述要複製之檔案的元素容器。 單一[transfermanifest](#syntax)節點底下可能包含多個[folderlist](#syntax)元素。

### <a name="syntax"></a>Syntax


```
<folderlist>
<!-- child elements -->
</folderlist>                 
                    
```



### <a name="attributes"></a>屬性

無。

### <a name="element-information"></a>項目資訊



| Parent 項目              | 子元素    |
|-----------------------------|-------------------|
| [transfermanifest](#syntax) | [資料夾](#syntax) |



 

## <a name="formdata"></a>formdata

描述可隨檔案傳送的選擇性 HTML 編碼表單資料。 如果它想要將檔案上傳為多部分的貼文，則服務會新增這個元素。 表單資料會連同 [post](#syntax) 元素中的資訊，用來建立貼文標頭。

單一[uploadinfo](#syntax)節點底下可能包含多個[formdata](#syntax)元素。

### <a name="syntax"></a>Syntax


```
<formdata
    name = "string"
>
<!-- child elements -->
</formdata>                   
                    
```



### <a name="attributes"></a>屬性



| 屬性 | 描述                                                                      |
|-----------|----------------------------------------------------------------------------------|
| NAME      | 必要。 定義與上傳區段相關聯的表單資料名稱。 |



 

### <a name="element-information"></a>項目資訊



| Parent 項目        | 子元素 |
|-----------------------|----------------|
| [uploadinfo](#syntax) | 無           |



 

## <a name="htmlui"></a>htmlui

當嚮導關閉時要顯示之伺服器端 HTML 頁面的 URL。 如果 [我的 [最愛](#syntax)] 專案不存在，且已指定上傳網站的易記名稱，此專案會在 [我的最愛 **]** 功能表中建立最愛的網頁

### <a name="syntax"></a>Syntax


```
<htmlui
    href = "string"
>
<!-- child elements -->
</htmlui>                 
                    
```



### <a name="attributes"></a>屬性



| 屬性 | 描述                                                                          |
|-----------|--------------------------------------------------------------------------------------|
| href      | 必要。 當嚮導關閉時要顯示之伺服器端 HTML 頁面的 URL。 |



 

### <a name="element-information"></a>項目資訊



| Parent 項目        | 子元素         |
|-----------------------|------------------------|
| [uploadinfo](#syntax) | 無。 允許文字。 |



 

## <a name="imageproperty"></a>imageproperty

指定與檔案相關的影像屬性。 單一[中繼資料](#syntax)節點下可包含多個[imageproperty](#syntax)元素。

### <a name="syntax"></a>Syntax


```
<imageproperty
    id = "string"
>
<!-- child elements -->
</imageproperty>                  
                    
```



### <a name="attributes"></a>屬性



| 屬性 | 描述                                  |
|-----------|----------------------------------------------|
| id        | 必要。 特定屬性的識別碼。 |



 

### <a name="element-information"></a>項目資訊



| Parent 項目      | 子元素         |
|---------------------|------------------------|
| [元](#syntax) | 無。 允許文字。 |



 

## <a name="metadata"></a>中繼資料

元素和文字的容器，用於定義特定檔案的中繼資料。 [單一檔案](#syntax)節點底下可能包含多個[中繼資料](#syntax)元素。

### <a name="syntax"></a>Syntax


```
<metadata>
<!-- child elements -->
</metadata>                   
                    
```



### <a name="attributes"></a>屬性

無。

### <a name="element-information"></a>項目資訊



| Parent 項目  | 子元素           |
|-----------------|--------------------------|
| [file](#syntax) | [imageproperty](#syntax) |



 

## <a name="netplace"></a>netplace

定義當上傳完成時，在 **我的網路位置** 中建立之網路位置的目標。 您可以透過 [**IPublishingWizard：： Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ipublishingwizard-initialize) 方法來防止建立網路位置。

### <a name="syntax"></a>Syntax


```
<netplace
    comment = "string"
    href = "string"
    name = "string"
>
<!-- child elements -->
</netplace>                   
                    
```



### <a name="attributes"></a>屬性



| 屬性 | 描述                                                                                     |
|-----------|-------------------------------------------------------------------------------------------------|
| comment   | 必要。 當游標停留在網路位置圖示上時，所顯示的批註。         |
| href      | 必要。 網路位置專案的 URL。                                                   |
| NAME      | 必要。 出現在 [ **我的網路位置** ] 資料夾中的網路位置圖示名稱。 |



 

### <a name="element-information"></a>項目資訊



| Parent 項目        | 子元素         |
|-----------------------|------------------------|
| [uploadinfo](#syntax) | 無。 允許文字。 |



 

## <a name="post"></a>post

應張貼檔案的 URL。 此專案是由服務在以多部分的 post 完成傳送時加入，且使用 [formdata](#syntax)來建立貼文標頭。 如果服務選擇使用 World Wide Web 分散式撰寫和版本設定來執行檔案傳輸 (WebDAV) ，它就不應該加入這個元素。 [單一檔案](#syntax)節點底下可能包含多個[post](#syntax)元素。

### <a name="syntax"></a>Syntax


```
<post
    filename = "string"
    href = "string"
    name = "string"
>
<!-- child elements -->
</post>                   
                    
```



### <a name="attributes"></a>屬性



| 屬性 | 說明                                                                    |
|-----------|--------------------------------------------------------------------------------|
| filename  | 選擇性。 張貼之檔案的檔案名。                                   |
| href      | 必要。 目的資料夾的 URL。                                   |
| NAME      | 必要。 定義與此貼文的這個區段相關聯的表單資料名稱。 |



 

### <a name="element-information"></a>項目資訊



| Parent 項目  | 子元素      |
|-----------------|---------------------|
| [file](#syntax) | [formdata](#syntax) |



 

## <a name="resize"></a>調整大小

以 JPEG 格式定義影像檔的縮放和 recompression。 如果來源檔案已為 JPEG 格式，且小於或等於指定的寬度和高度，則不會調整大小。 如果來源檔案不是 JPEG 檔案，則會進行轉換。 您可以透過 [**IPublishingWizard：： Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ipublishingwizard-initialize) 方法防止調整、recompression 和轉換檔案。 [單一檔案](#syntax)節點底下可能包含多個重[設大小](#syntax)的元素。

### <a name="syntax"></a>Syntax


```
<resize
    cx = "string"
    cy = "string"
    quality = "string"
>
<!-- child elements -->
</resize>                 
                    
```



### <a name="attributes"></a>屬性



| 屬性 | 描述                                                                                                                                                         |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 殘雪        | 必要。 上傳之後影像的寬度（以圖元為單位）。 如果這個值為0，則會從 **cy** 值計算 **cx** 以保留相對維度。  |
| cy        | 必要。 上傳之後影像的高度（以圖元為單位）。 如果這個值為0，則會從 **cx** 值計算 **cy** 以保留相對維度。 |
| 品質   | 必要。 JPEG 品質值（介於0和100之間），100為最高品質。                                                                            |



 

### <a name="element-information"></a>項目資訊



| Parent 項目  | 子元素 |
|-----------------|----------------|
| [file](#syntax) | 無。          |



 

## <a name="successpage"></a>successpage

指定當上傳成功時，要顯示的伺服器端 HTML 頁面。

### <a name="syntax"></a>Syntax


```
<successpage
    href = "string"
>
<!-- child elements -->
</successpage>                    
                    
```



### <a name="attributes"></a>屬性



| 屬性 | 描述                                                                            |
|-----------|----------------------------------------------------------------------------------------|
| href      | 必要。 當上傳成功時，要顯示之伺服器端 HTML 頁面的 URL。 |



 

### <a name="element-information"></a>項目資訊



| Parent 項目        | 子元素         |
|-----------------------|------------------------|
| [uploadinfo](#syntax) | 無。 允許文字。 |



 

## <a name="target"></a>目標

以通用命名慣例指定的目的資料夾 (UNC) 格式或 WebDAV 伺服器。 如果傳送使用 WebDAV 或檔案系統通訊協定，則服務會新增這個目標來指定目的地資料夾。 如果服務選擇以多部分 post 的方式執行檔案傳輸，則不應新增此元素。

### <a name="syntax"></a>Syntax


```
<target
    href = "string"
>
<!-- child elements -->
</target>                 
                    
```



### <a name="attributes"></a>屬性



| 屬性 | 描述                                                                                                                 |
|-----------|-----------------------------------------------------------------------------------------------------------------------------|
| href      | 必要。 目的資料夾的 URL。 針對 WebDAV 使用 **HTTPs://** 格式，或針對 UNC 使用 **\\ \\ 伺服器 \\ 共用** 表單。 |



 

### <a name="element-information"></a>項目資訊



| Parent 項目        | 子元素         |
|-----------------------|------------------------|
| [uploadinfo](#syntax) | 無。 允許文字。 |



 

## <a name="transfermanifest"></a>transfermanifest

傳送資訊清單檔案的父節點。

### <a name="syntax"></a>Syntax


```
<transfermanifest>
<!-- child elements -->
</transfermanifest>                   
                    
```



### <a name="attributes"></a>屬性

無。

### <a name="element-information"></a>項目資訊



| Parent 項目 | 子元素                                                    |
|----------------|-------------------------------------------------------------------|
| 無           | [filelist](#syntax)、 [folderlist](#syntax)、 [uploadinfo](#syntax) |



 

## <a name="uploadinfo"></a>uploadinfo

專案的容器，可從交易中使用的上傳網站提供資訊。 單一[transfermanifest](#syntax)節點底下可能包含多個[uploadinfo](#syntax)元素。

### <a name="syntax"></a>Syntax


```
<uploadinfo
    friendlyname = "string"
>
<!-- child elements -->
</uploadinfo>                 
                    
```



### <a name="attributes"></a>屬性



| 屬性    | 描述                                                                 |
|--------------|-----------------------------------------------------------------------------|
| 友好 | 必要。 網站的易記名稱，此名稱會顯示在嚮導中。 |



 

### <a name="element-information"></a>項目資訊



| Parent 項目              | 子元素                                                                                                                                           |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [transfermanifest](#syntax) | [cancelledpage](#syntax)、 [failurepage](#syntax)、我的 [最愛](#syntax)、 [htmlui](#syntax)、 [netplace](#syntax)、 [successpage](#syntax)、 [target](#syntax) |



 

 

 



