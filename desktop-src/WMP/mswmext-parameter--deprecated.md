---
title: " (已淘汰的 MSWMExt 參數) "
description: " (已淘汰的 MSWMExt 參數) "
ms.assetid: cc52da1a-26d1-4321-b421-b0d6f44635cc
keywords:
- Windows Media 中繼檔，MSWMExt 參數
- 中繼檔，MSWMExt 參數
- MSWMExt 參數
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 745ecfb2cf716e973aec3d574247e3e45d8f49ff
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104374626"
---
# <a name="mswmext-parameter-deprecated"></a><span data-ttu-id="1fd2c-106"> (已淘汰的 MSWMExt 參數) </span><span class="sxs-lookup"><span data-stu-id="1fd2c-106">MSWMExt Parameter (deprecated)</span></span>

<span data-ttu-id="1fd2c-107">*MSWMExt* 參數會向用戶端程式指出參考檔案的格式。</span><span class="sxs-lookup"><span data-stu-id="1fd2c-107">The *MSWMExt* parameter indicates to a client program the format of a referenced file.</span></span>

<span data-ttu-id="1fd2c-108">**語法**</span><span class="sxs-lookup"><span data-stu-id="1fd2c-108">**Syntax**</span></span>


```XML

URL?MSWMExt=.
ext
```



<span data-ttu-id="1fd2c-109">**範例程式碼**</span><span class="sxs-lookup"><span data-stu-id="1fd2c-109">**Example Code**</span></span>


```XML
[reference]
Ref01 = https://example.com/GenerateASFFile.aspx?MSWMExt=.asf

```



## <a name="remarks"></a><span data-ttu-id="1fd2c-110">備註</span><span class="sxs-lookup"><span data-stu-id="1fd2c-110">Remarks</span></span>

<span data-ttu-id="1fd2c-111">用戶端程式有時會使用副檔名或 MIME 類型來判斷是否要將媒體檔案轉譯為數據流、在完整下載之後轉譯檔案，或拒絕轉譯檔案。</span><span class="sxs-lookup"><span data-stu-id="1fd2c-111">Client programs sometimes use a file name extension or a MIME type to determine whether to render a media file as a stream, render the file after a full download, or refuse to render the file at all.</span></span> <span data-ttu-id="1fd2c-112">如果用戶端程式無法判斷如何根據副檔名或 MIME 類型來處理媒體檔案，它可以藉由檢查 *MSWMExt* 參數來判斷如何處理檔案。</span><span class="sxs-lookup"><span data-stu-id="1fd2c-112">If a client program cannot determine how to treat a media file based on the file name extension or the MIME type, it can determine how to treat the file by inspecting the *MSWMExt* parameter.</span></span> <span data-ttu-id="1fd2c-113">例如，用戶端可以將檔案視為具有等於 *MSWMExt* 參數值的副檔名。</span><span class="sxs-lookup"><span data-stu-id="1fd2c-113">For example, the client could treat the file as if it had an extension equal to the value of the *MSWMExt* parameter.</span></span> <span data-ttu-id="1fd2c-114">如需有關 MIME 類型與 [副檔名的詳細](file-name-extensions.md)資訊，請參閱副檔名。</span><span class="sxs-lookup"><span data-stu-id="1fd2c-114">For more information about MIME types and file name extensions, see [File Name Extensions](file-name-extensions.md).</span></span> <span data-ttu-id="1fd2c-115">如需 *MSWMExt* 參數的詳細資訊，請參閱 Microsoft 知識庫中的文章 [236895](https://support.microsoft.com/kb/236895) 。</span><span class="sxs-lookup"><span data-stu-id="1fd2c-115">For more information about the *MSWMExt* parameter, see article [236895](https://support.microsoft.com/kb/236895) in the Microsoft Knowledge Base.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1fd2c-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="1fd2c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fd2c-117">**舊版的 Windows Media 中繼檔 (已淘汰)**</span><span class="sxs-lookup"><span data-stu-id="1fd2c-117">**Previous Versions of Windows Media Metafiles (deprecated)**</span></span>](previous-versions-of-windows-media-metafiles--deprecated.md)
</dt> </dl>

 

 




