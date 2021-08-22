---
title: '自訂字型集合 (Windows 7/8) '
description: DirectWrite 使用 IDWriteFactory GetSystemFontCollection 方法提供系統字型集合的存取權。
ms.assetid: ec892904-6778-4fbd-93b4-62d0db5b82ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffc76214dda067b43c27c8e04e4419f147d0e33b7566b4dedc5ac3255a1c1dc9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290758"
---
# <a name="custom-font-collections-windows-78"></a>自訂字型集合 (Windows 7/8) 

[DirectWrite](direct-write-portal.md)使用 [**IDWriteFactory：： GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection)方法提供系統字型集合的存取權。 這是最常使用的字型集合。 不過，有些應用程式必須使用系統上未安裝的字型，例如從包含的字型檔案或內嵌于應用程式中的字型檔案。

如果您想要的字型不在系統字型集合中，您可以建立衍生自 [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection)的自訂字型集合。

此總覽包含下列部分：

-   [註冊和取消註冊字型集合載入器](#registering-and-unregistering-a-font-collection-loader)
-   [IDWriteFontCollectionLoader](#idwritefontcollectionloader)
-   [IDWriteFontFileEnumerator](#idwritefontfileenumerator)
-   [CreateCustomFontFileReference](#createcustomfontfilereference)
-   [IDWriteFontFileLoader](#idwritefontfileloader)
-   [IDWriteFontFileStream](#idwritefontfilestream)

## <a name="registering-and-unregistering-a-font-collection-loader"></a>註冊和取消註冊字型集合載入器

您可以使用 [**IDWriteFactory：： RegisterFontCollectionLoader**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-registerfontcollectionloader) 方法來註冊字型集合載入器，並將應用程式實作為單一物件的 [**IDWriteFontCollectionLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollectionloader) 介面傳遞給它。 當要求自訂集合時，這個物件會載入字型。 系統字型集合和自訂字型集合都會進行快取，因此只會載入一次字型。

字型集合載入器最後必須使用 [**IDWriteFactory：： UnregisterFontCollectionLoader**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-unregisterfontcollectionloader)卸載。

> [!Note]  
> 註冊字型集合載入器會新增至參考計數;請勿從函式內呼叫 [**UnregisterFontCollectionLoader**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-unregisterfontcollectionloader) ，否則將永遠不會取消註冊集合載入器物件。

 

## <a name="idwritefontcollectionloader"></a>IDWriteFontCollectionLoader

您可以使用 [**IDWriteFactory：： CreateCustomFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontcollection)建立 [**IDWriteFontFileEnumerator**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileenumerator)物件，並將它傳遞至應用程式定義的索引鍵。 索引鍵是 void 指標，而資料類型、格式和意義是由應用程式所定義，而且對字型系統而言是不透明的。

索引鍵可以是任何內容， [DirectWrite](direct-write-portal.md)要求每個金鑰都必須是：

-   在載入器範圍內的單一字型集合中是唯一的。
-   在使用 factory 取消註冊載入器之前有效。

呼叫 [**CreateCustomFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontcollection)方法時， [DirectWrite](direct-write-portal.md)會呼叫回 [**IDWriteFontCollectionLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollectionloader)介面，應用程式會將它實作為單一物件。 [**IDWriteFontCollectionLoader：： CreateEnumeratorFromKey**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollectionloader-createenumeratorfromkey)回呼方法是由 DirectWrite 用來取出應用程式所執行的 [**IDWriteFontFileEnumerator**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileenumerator)物件。 用來建立集合的 [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) 物件會傳遞給這個方法，且應該由字型檔案列舉值用來建立要包含在集合中的 [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) 物件。

傳遞給這個方法的金鑰會識別字型集合，而且是傳遞給 [**CreateCustomFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontcollection)的相同索引鍵。

## <a name="idwritefontfileenumerator"></a>IDWriteFontFileEnumerator

[**CreateEnumeratorFromKey**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollectionloader-createenumeratorfromkey)方法所建立的應用程式定義 [**IDWriteFontFileEnumerator**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileenumerator)物件是用來列舉集合中的字型檔案，為每個檔案建立 [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile)物件。 [**IDWriteFontFileEnumerator：： MoveNext**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-movenext)方法會將位置變更為下一個字型檔案。 如果位置有檔案，則會將 *hasCurrentFile* 設為 **TRUE**。 否則，它會設為 **FALSE** ，而且方法會傳回 **S \_ OK**。

> [!Note]  
> 字型檔案列舉值的開頭必須是在第一個元素之前，並在第一次呼叫 [**MoveNext**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-movenext)時開始。

 

[**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile)物件是由 [**IDWriteFontFileEnumerator：： GetCurrentFontFile**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-getcurrentfontfile)方法輸出。 如果目前位置沒有字型檔案，因為 [**MoveNext**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-movenext) 尚未呼叫或 hasCurrentFile 設定為 **FALSE**，則 **GetCurrentFontFile** 會傳回 **E \_ 失敗**。

## <a name="createcustomfontfilereference"></a>CreateCustomFontFileReference

藉由呼叫 [**IDWriteFactory：： CreateCustomFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontfilereference)，即可建立 [**GetCurrentFontFile**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-getcurrentfontfile)的 [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile)物件輸出。 字型檔案參考索引鍵會識別特定的字型檔案參考，且在載入檔案的字型檔案載入器中必須是唯一的。

## <a name="idwritefontfileloader"></a>IDWriteFontFileLoader

[**CreateCustomFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontfilereference)方法會採用應用程式所執行的 [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader)物件，此物件是用來載入字型。 [**IDWriteFontFileLoader：： CreateStreamFromKey**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileloader-createstreamfromkey)回呼方法會傳遞金鑰，並輸出 [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream)物件。

## <a name="idwritefontfilestream"></a>IDWriteFontFileStream

應用程式所執行的 [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) 物件會從自訂字型檔案載入器提供字型檔案參考的字型檔案資料。 除了檔案大小和上次寫入時間，它也提供方法 ([**ReadFileFragment**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfilestream-readfilefragment)) ，以抓取要編譯成 [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) 物件的檔案片段。

> [!Note]  
> 如果要求的片段超出檔案範圍， [**ReadFileFragment**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfilestream-readfilefragment)的執行應該會傳回錯誤。

 

[**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream)可以從任何地方取得字型檔案內容，例如本機硬碟或內嵌的資源。

 

 