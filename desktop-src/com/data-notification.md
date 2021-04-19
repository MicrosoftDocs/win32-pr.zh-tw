---
title: 資料通知
description: 當來源中的資料變更時，使用來自外部來源之資料的物件有時需要獲得通知。
ms.assetid: 286a1ecf-5255-4443-a17d-5ffa55ed0be1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49df9e6bb7d9b15192473b18114fe7fcd69ecedf
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106990898"
---
# <a name="data-notification"></a>資料通知

當來源中的資料變更時，使用來自外部來源之資料的物件有時需要獲得通知。 例如，以某些試算表中資料為依據的股票行情，需要在資料變更時收到通知，讓它可以更新其顯示。 同樣地，複合檔案需要其内嵌物件中資料變更的相關資訊，使其可以更新其資料快取。 在這種情況下，需要動態更新資料的情況下，資料來源需要一些機制來通知資料取用者發生變更，而不強制取用者來捨棄所有專案，以便更新其資料。 在理想的情況下，會在資料來源中收到變更的通知，取用的物件可在其休閒時要求更新的複本。

用來處理這種類型之非同步通知的 COM 機制，就是稱為「建議接收」的物件，它只是任何會實 [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink)介面的 com 物件。 資料的取用者會執行 **IAdviseSink**。 他們會藉由將指標傳給感興趣的資料物件來進行註冊，以接收通知。

[**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink)介面會公開下列用來接收非同步通知的方法：



| 方法                                                      | 通知通知接收                                            |
|-------------------------------------------------------------|--------------------------------------------------------------------------|
| [**OnDataChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-ondatachange)<br/> | 呼叫物件的資料已經變更。<br/>                        |
| [**OnViewChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onviewchange)<br/> | 繪製呼叫物件的指示已經變更。<br/> |
| [**OnRename**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onrename)<br/>         | 呼叫物件的標記已變更。<br/>                     |
| [**OnSave**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onsave)<br/>             | 呼叫物件已儲存至持續性儲存體。<br/>      |
| [**OnClose**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onclose)<br/>           | 呼叫物件已關閉。<br/>                           |



 

如資料表所示， [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) 介面會公開方法，以在呼叫物件資料中的變更以外，通知通知接收的事件。 呼叫物件也可以在其繪製本身變更的方式中通知接收，或是重新命名、儲存或關閉。 這些其他通知主要是在複合檔案的內容中使用，雖然通知機制相同。 如需複合檔案通知的詳細資訊，請參閱「複合檔案」。

為了充分利用「建議」接收，資料來源必須執行 [**IDataObject：:D 的建議**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-dadvise)、 [**IDataObject：:D unadvise**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-dunadvise)和 [**IDataObject：： EnumDAdvise**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumdadvise)。 資料取用者會呼叫 **DAdvise** mothod 來通知資料物件，以便在物件的資料變更時收到通知。 取用物件會呼叫 **DUnadvise** 方法來卸載此連接。 任何有興趣的合作物件都可以呼叫 **EnumDAdvise** 方法，以瞭解具有資料物件之諮詢連接的物件數目。

當資料在來源上變更時，資料物件會在已註冊要接收通知的所有資料取用者上呼叫 [**IAdviseSink：： OnDataChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-ondatachange) 。 為了追蹤諮詢連接，以及管理通知分派，資料來源會依賴稱為 *資料建議者* 的物件。 您可以藉由執行 [**IDataAdviseHolder**](/windows/desktop/api/ObjIdl/nn-objidl-idataadviseholder) 介面來建立您自己的資料建議者。 或者，您可以藉由呼叫 helper 函數 [**CreateDataAdviseHolder**](/windows/win32/api/ole2/nf-ole2-createdataadviseholder)，讓 COM 為您完成。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[資料轉送](data-transfer.md)
</dt> </dl>

 

