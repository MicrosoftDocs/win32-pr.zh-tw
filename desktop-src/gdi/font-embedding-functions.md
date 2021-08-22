---
description: 下列函式會搭配內嵌 Microsoft OpenType 字型使用。
ms.assetid: 8f47d7a5-db45-4a41-8af2-9fc6b373a531
title: 字型嵌入函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fe820c8b9e6a17f148705599d77ea08bbc4b3f8d52821c171c9e86ca13e2ad1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118761181"
---
# <a name="font-embedding-functions"></a>字型嵌入函式

下列函式會搭配內嵌 Microsoft OpenType 字型使用。



| 函式                                                                   | 描述                                                                                                                                              |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*CFP \_ ALLOCPROC*](/windows/desktop/api/FontSub/nc-fontsub-cfp_allocproc)                                      | 適用于 CreateFontPackage 和 MergeFontPackage 的應用程式提供記憶體配置函數。                                                              |
| [*CFP \_ FREEPROC*](/windows/desktop/api/FontSub/nc-fontsub-cfp_freeproc)                                        | CreateFontPackage 和 MergeFontPackage 的應用程式提供的記憶體解除配置函數。                                                            |
| [*CFP \_ REALLOCPROC*](/windows/desktop/api/FontSub/nc-fontsub-cfp_reallocproc)                                  | 應用程式提供的 CreateFontPackage 和 MergeFontPackage 記憶體重新配置函數。                                                            |
| [**CreateFontPackage**](/windows/desktop/api/FontSub/nf-fontsub-createfontpackage)                             | 為指定的 TrueType 字型建立更精簡的版本，以便將其傳遞至印表機。 產生的字型可能會有子集、已壓縮或兩者。 |
| [**MergeFontPackage**](/windows/desktop/api/FontSub/nf-fontsub-mergefontpackage)                               | 合併 CreateFontPackage 所建立的子集字型。                                                                                                        |
| [*READEMBEDPROC*](/previous-versions//dd162894(v=vs.85))                                       | 用戶端提供的回呼函式，可從緩衝區讀取串流內容。                                                                                 |
| [**TTCharToUnicode**](/windows/desktop/api/T2embapi/nf-t2embapi-ttchartounicode)                                 | 將8位字元碼值的陣列轉換成16位的 Unicode 值。                                                                               |
| [**TTDeleteEmbeddedFont**](/windows/desktop/api/T2embapi/nf-t2embapi-ttdeleteembeddedfont)                       | 釋放內嵌字型所使用的記憶體。                                                                                                                |
| [**TTEmbedFont**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfont)                                         | 使用裝置內容做為字型內嵌資訊來源，建立包含子集寬字元 (16 位) 字型的字型結構。           |
| [**TTEmbedFontEx**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfontex)                                     | 使用裝置內容做為字型內嵌資訊來源，建立包含已子集的 UCS-4 字元 (32 位) 字型的字型結構。        |
| [**TTEmbedFontFromFileA**](/windows/desktop/api/T2embapi/nf-t2embapi-ttembedfontfromfilea)                       | 使用檔案作為字型內嵌資訊來源，建立包含已子集寬字元 (16 位) 字型的字型結構。                     |
| [**TTEnableEmbeddingForFacename**](/windows/desktop/api/T2embapi/nf-t2embapi-ttenableembeddingforfacename)       | 新增或移除字體排除清單中的 facenames。                                                                                              |
| [**TTGetEmbeddedFontInfo**](/windows/desktop/api/T2embapi/nf-t2embapi-ttgetembeddedfontinfo)                     | 抓取內嵌字型的相關資訊。                                                                                                            |
| [**TTGetEmbeddingType**](/windows/desktop/api/T2embapi/nf-t2embapi-ttgetembeddingtype)                           | 傳回字型的內嵌許可權。                                                                                                                  |
| [**TTGetNewFontName**](/windows/desktop/api/T2embapi/nf-t2embapi-ttgetnewfontname)                               | 針對已安裝的內嵌字型建立新的名稱。                                                                                                       |
| [**TTIsEmbeddingEnabled**](/windows/desktop/api/T2embapi/nf-t2embapi-ttisembeddingenabled)                       | 判斷字體排除清單是否包含指定的字型。                                                                                     |
| [**TTIsEmbeddingEnabledForFacename**](/windows/desktop/api/T2embapi/nf-t2embapi-ttisembeddingenabledforfacename) | 判斷是否已啟用指定字型的內嵌。                                                                                            |
| [**TTLoadEmbeddedFont**](/windows/desktop/api/T2embapi/nf-t2embapi-ttloadembeddedfont)                           | 從檔資料流程讀取內嵌的字型，並加以安裝。 也可讓用戶端進一步限制字型的內嵌許可權。             |
| [**TTRunValidationTests**](/windows/desktop/api/T2embapi/nf-t2embapi-ttrunvalidationtests)                       | 在指定的大小範圍內，驗證寬字元 (16 位) 字型的部分或所有字元資料。                                                         |
| [**TTRunValidationTestsEx**](/windows/desktop/api/T2embapi/nf-t2embapi-ttrunvalidationtestsex)                   | UCS-4 版本的 TTRunValidationTests。                                                                                                                   |
| [*WRITEEMBEDPROC*](/previous-versions//dd145225(v=vs.85))                                     | 用戶端提供的回呼函式，可將資料流程內容寫入緩衝區。                                                                                  |



 

 

 
