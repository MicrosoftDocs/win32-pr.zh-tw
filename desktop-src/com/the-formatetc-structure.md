---
title: FORMATETC 結構
description: FORMATETC 結構是一般化剪貼簿格式，已增強以包含目標裝置、資料的外觀或觀點，以及儲存媒體。
ms.assetid: 46d8988a-4b97-4c86-8b1b-db87044a7e01
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ece0079cf2c0f07b7356f07ee2c53b1279b7ce7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683168"
---
# <a name="the-formatetc-structure"></a>FORMATETC 結構

FORMATETC 結構是一般化剪貼簿格式，已增強以包含目標裝置、資料的 *外觀* 或觀點，以及儲存媒體。 資料取用者（例如 OLE 容器應用程式）會在對 [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)的呼叫中將 [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc)結構傳遞為引數，以表示它想要從資料來源（例如複合檔案物件）的資料類型。 來源會使用 **FORMATETC** 結構來描述它可提供的格式。

[**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) 可以描述幾乎所有資料，包括其他物件（例如，例如名字）。 容器可以呼叫 [**IDataObject：： EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc)來要求其中一個内嵌物件來列出其資料格式，以傳回可執行 [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) 介面的列舉值物件。 而不是只回復它有「文字和點陣圖」。物件可以提供資料的詳細說明，包括裝置 (通常呈現的螢幕或印表機) 、呈現給使用者的外觀 (完整的內容、縮圖、圖示或列印) 的格式，以及包含資料 (全域記憶體、磁片檔案、儲存物件或串流) 的儲存媒體。 這項能夠緊密描述資料的功能，會導致高品質的印表機和螢幕輸出，以及更有效率的資料流覽，其中縮圖草圖的抓取和顯示速度會比完整的呈現更快。

下表列出 [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) 資料結構的欄位，以及它們所指定的資訊。



| 欄位                   | 指定                                                                                                                                                                                                                                                                    |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **cfFormat**<br/> | 轉譯資料的格式，可以是標準剪貼簿格式、專屬格式或 OLE 格式。 如需有關 OLE 格式的詳細資訊，請參閱 [複合檔案](compound-documents.md)。<br/>                                          |
| **ptd**<br/>      | [**DVTARGETDEVICE**](/windows/win32/api/objidl/ns-objidl-dvtargetdevice)結構，其中包含與 Windows 目標裝置相關的足夠資訊（例如螢幕或印表機），因此可以使用 [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca)函式來建立其裝置內容的控制碼 (hDC) 。 <br/> |
| **dwAspect**<br/> | 要呈現之資料的外觀或觀點;可以是完整的內容、縮圖草圖、圖示，或格式化以進行列印。<br/>                                                                                                                                  |
| **lindex**<br/>   | 感興趣的層面部分;目前，此值必須是-1，表示會有興趣的整個觀點。<br/>                                                                                                                                |
| **tymed**<br/>    | 資料的儲存媒體，可以是全域記憶體、磁片檔案或其中一個 COM 結構儲存介面的實例。<br/>                                                                                                                                   |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[資料格式和傳輸媒體](data-formats-and-transfer-media.md)
</dt> </dl>

 

