---
title: 資料傳輸介面
description: 資料傳輸介面
ms.assetid: c42e65a4-7b77-4f39-8323-04fa60c5b140
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 448e1a580880c7202ec67d12965f6db7e0be99d0
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106967499"
---
# <a name="data-transfer-interfaces"></a>資料傳輸介面

[**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)介面為數據取用者提供了取得及設定物件資料的方法、判斷物件所支援的格式，以及在物件中的資料變更時，註冊和接收通知。 取得資料時，呼叫端可以指定要用來呈現資料的格式。 但是，資料的來源會判斷儲存媒體，它會在呼叫端所提供的 out 參數中傳回。

[**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)本身會提供在您的應用程式中執行 Windows 剪貼簿傳輸或複合檔案傳輸所需的所有工具。 如果您也想要支援拖放傳輸，您需要執行 [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) 和 [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) 介面以及 **IDataObject**。

[**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)介面與 OLE 剪貼簿 api 結合，可提供 Windows 剪貼簿 api 的所有功能。 通常不需要同時使用剪貼簿 Api。 支援拖放傳送或 OLE 複合檔案的資料供應商必須執行 **IDataObject** 介面。 如果您的應用程式現在僅支援剪貼簿傳送，但您想要在稍後的版本中新增拖放或複合檔案，您可能會想要立即執行 **IDataObject** 和 OLE 剪貼簿 api，以將稍後進行編碼和偵測所花費的時間降到最低。 您也可能想要執行 **IDataObject** ，以便利用全域記憶體以外的傳輸媒體。

下表摘要說明要使用的資料，視您要支援的資料傳輸類型而定：



| 若要支援                                                                       | 使用                                                                                                                                                                         |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 複合檔案<br/>                                                    | [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)<br/>                                                                                                                               |
| 拖放傳送<br/>                                               | [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)、 [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource)、 [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget)、 [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) (或相等的) <br/> |
| 以獨佔方式使用全域記憶體傳送剪貼簿<br/>                   | [剪貼簿 API](../dataxchg/clipboard.md)<br/>                                                                                                                            |
| 使用全域記憶體以外的 exchange 媒體傳送剪貼簿。<br/>  | [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)<br/>                                                                                                                               |
| 剪貼簿立即傳送，但稍後再拖放或複合檔案<br/> | [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) 和上面列出的「拖放傳輸」的介面和功能<br/>                                                    |



 

當使用者啟動資料傳輸作業時，來源應用程式會建立 [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) 的實例，並透過它來提供一或多個格式的資料。 在「剪貼簿」傳送中，應用程式會呼叫 [**OleSetClipboard**](/windows/desktop/api/Ole2/nf-ole2-olesetclipboard) 函式，將資料物件指標傳遞給 OLE。  (**OleSetClipboard** 也提供 OLE 版本1和非 OLE 應用程式的標準剪貼簿資料格式。在拖放傳輸中 ) ，應用程式會改為呼叫 [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) 函式。

在傳送的接收端，目的地會接收 [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) 指標做為 IDropTarget 的調用的引數 [**：:D Rop**](/windows/desktop/api/OleIdl/nf-oleidl-idroptarget-drop) 或呼叫 [**OleSetClipboard**](/windows/desktop/api/Ole2/nf-ole2-olesetclipboard) 函式，取決於是否透過拖放或剪貼簿來傳送。 取得此指標之後，目的地會呼叫 [**IDataObject：： EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc) 來瞭解哪些格式可供抓取，以及可以取得哪些類型的媒體。 透過此資訊，接收應用程式會透過呼叫 [**IDataObject：：**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata)來要求資料。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[資料轉送](data-transfer.md)
</dt> </dl>

 

