---
description: 本節說明如何藉由呼叫動態連結程式庫或腳本，從實際執行一部分安裝的自訂動作傳送訊息。
ms.assetid: 637efccf-920d-421d-9183-528cc3515bf8
title: 從自訂動作傳回錯誤訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c951b0e86d3120b989605572f15681582ac437fca5981852413331a3e63e684
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869118"
---
# <a name="returning-error-messages-from-custom-actions"></a>從自訂動作傳回錯誤訊息

本節說明如何藉由呼叫動態連結程式庫或腳本，從實際執行一部分安裝的自訂動作傳送訊息。 請注意， [自訂動作類型 19](custom-action-type-19.md) 只會傳送指定的錯誤訊息、傳回失敗，然後結束安裝。 自訂動作類型19不會執行安裝的任何部分。

若要從使用 [動態連結程式庫](dynamic-link-libraries.md) (DLL) 的自訂動作傳送錯誤訊息，請使用自訂動作呼叫 [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage)。 請注意， [Dataadapter.doaction ControlEvent](doaction-controlevent.md) 啟動的自訂動作可以使用 [**Message**](session-message.md) 方法傳送訊息，但無法使用 **MsiProcessMessage** 傳送訊息。 在 Windows Server 2003 之前的系統上，由 dataadapter.doaction ControlEvent 啟動的自訂動作無法使用 **MsiProcessMessage** 或 **Message** 方法傳送訊息。 如需詳細資訊，請參閱[使用 MsiProcessMessage 將訊息傳送至 Windows Installer](sending-messages-to-windows-installer-using-msiprocessmessage.md)。

**使用 DLL 在自訂動作內顯示錯誤訊息**

1.  自訂動作應該會呼叫 [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) ，並傳入 *hInstall*、 *eMessageType* 和 *hRecord* 參數。 [從自訂動作或 MsiOpenProduct 或 MsiOpenPackage 存取目前的安裝程式會話](accessing-the-current-installer-session-from-inside-a-custom-action.md)中所述，可將安裝的控制碼（[自訂動作類型 19](custom-action-type-19.md)）提供給[](/windows/desktop/api/Msi/nf-msi-msiopenproducta)自訂[](/windows/desktop/api/Msi/nf-msi-msiopenpackagea)動作。
2.  參數 *eMessageType* 應指定其中一種訊息類型，如 [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage)中所列。
3.  [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage)函數的 *hRecord* 參數會根據訊息類型而定。 請參閱[使用 MsiProcessMessage 將訊息傳送至 Windows Installer](sending-messages-to-windows-installer-using-msiprocessmessage.md)。 如果訊息包含格式化的資料，請使用 [[格式化](formatted.md)] 中所述的格式，將訊息輸入[錯誤](error-table.md)資料表。

若要從使用 [腳本](scripts.md)的自訂動作傳送錯誤訊息，自訂動作可能會呼叫 [**會話**](session-object.md)物件的 [**訊息**](session-message.md)方法。

**使用腳本在自訂動作中顯示錯誤訊息**

1.  自訂動作應呼叫 [**會話**](session-object.md)物件的 [**訊息**](session-message.md)方法，並傳入參數 *種類* 和 *記錄*。
2.  參數 *種類* 應該指定 [**訊息**](session-message.md) 方法中所列的其中一種訊息類型。
3.  [**Message**](session-message.md)方法的 *record* 參數會根據訊息類型而定。 如果訊息包含格式化的資料，請使用 [[格式化](formatted.md)] 中所述的格式，將訊息輸入[錯誤](error-table.md)資料表。

使用 [可執行檔](executable-files.md) 的自訂動作無法藉由呼叫 [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) 或 [**message**](session-message.md) 方法來傳送訊息，因為它們無法取得安裝的控制碼。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[自訂動作傳回值](custom-action-return-values.md)
</dt> </dl>

 

 



