---
title: '内嵌物件 (文字服務架構) '
description: 文字服務架構可讓文字服務將物件內嵌在應用程式文字資料流程中。
ms.assetid: 44cb22b5-707b-4f21-b986-5258ed273543
keywords:
- 文字服務架構 (TSF) 的内嵌物件
- TSF (文字服務架構) ，内嵌物件
- 啟用 TSF 的應用程式，内嵌物件
- 內嵌物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39e4f819e6f42cc4e8d2ed81e47c79efe5ff7407
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104556833"
---
# <a name="embedded-objects-text-services-framework"></a>内嵌物件 (文字服務架構) 

文字服務架構可讓文字服務將物件內嵌在應用程式文字資料流程中。 内嵌物件會使用值 [TS \_ 字元 \_ 內嵌](ts-char--constants.md)來插入文字資料流程中。 這個值會使用十六進位標記法解析為 Unicode 物件取代字元 U + fffc。 例如，下圖顯示的是代表日文漢字（ *hi*）的内嵌物件轉譯，結合 Unicode 字元序列（代表 "Sun" 的英文翻譯）。

![内嵌物件的字元編碼](images/emb-obj.gif)

圖頂端的資料列包含翻譯的文字，其中包含 "Sun" 一 *字，後面* 接著 Sun 的日文字元。 此圖的中間資料列會顯示 Unicode 字元。 在 U + fffc 的案例中，這是物件取代字元。 圖底部的資料列顯示每個字元的十六進位值。

## <a name="supporting-embedded-objects-in-an-application"></a>支援應用程式中的内嵌物件

TSF manager 會針對 ACP 型應用程式呼叫 [ITextStoreACP：： InsertEmbedded](/windows/desktop/api/textstor/nf-textstor-itextstoreacp-insertembedded) ，將内嵌物件插入至文字資料流程，或針對錨點應用程式呼叫 [ITextStoreAnchor：： InsertEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembedded) 。 插入内嵌物件時，應用程式應該將 **TS \_ 字元 \_ 內嵌** 值放在 IDataObject 物件的字元 (位置，或錨點位置) ，並儲存與内嵌物件相關聯的。 當呼叫 [ITextStoreACP：： GetText](/windows/desktop/api/textstor/nf-textstor-itextstoreacp-gettext) 或 [ITextStoreAnchor：： GetText](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-gettext) ，且内嵌物件包含在取得的文字內時， **TS \_ 字元 \_ 內嵌** 值會指出内嵌物件的存在和位置。 若要取得内嵌物件，請以内嵌物件的字元位置呼叫 [ITextStoreACP：： GetEmbedded](/windows/desktop/api/textstor/nf-textstor-itextstoreacp-getembedded) ，或使用内嵌物件的錨點位置來呼叫 [ITextStoreAnchor：： GetEmbedded](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getembedded) 。

應用程式通常不會辨識内嵌物件的內容。 應用程式可以嘗試從物件本身取得顯示資訊。 如果内嵌物件可以提供應用程式可辨識的格式資料，例如 CF \_ UNICODETEXT 或 cf \_ 點陣圖，則應用程式可以顯示物件所提供的圖形資訊。

## <a name="inserting-embedded-objects"></a>插入內嵌物件

文字服務會藉由呼叫 [ITfRange：： InsertEmbedded](/windows/desktop/api/msctf/nf-msctf-itfrange-insertembedded) 或 [ITfInsertAtSelection：： InsertEmbeddedAtSelection](/windows/desktop/api/msctf/nf-msctf-itfinsertatselection-insertembeddedatselection)，將内嵌物件插入內容中。 文字服務必須提供內嵌的 IDataObject。

 

 
