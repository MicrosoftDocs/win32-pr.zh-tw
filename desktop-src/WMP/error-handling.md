---
title: 處理 (Windows Media Player SDK) 時發生錯誤
description: 錯誤處理
ms.assetid: f0567c77-a855-4b93-9fb7-a36cde63859f
keywords:
- Windows Media Player，錯誤處理
- Windows Media Player 物件模型、錯誤處理
- 物件模型、錯誤處理
- Windows Media Player ActiveX 控制項，錯誤處理
- ActiveX 控制項，錯誤處理
- Windows Media Player 的行動 ActiveX 控制項、錯誤處理
- Windows Media Player 行動電話，錯誤處理
- 遷移指南，錯誤處理
- 物件模型中的錯誤處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f3b96e04d24009ee4b7e5819fdb26dfd6effd63
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104093576"
---
# <a name="error-handling-windows-media-player-sdk"></a>處理 (Windows Media Player SDK) 時發生錯誤

Windows Media Player 6.4 ActiveX 控制項藉由在對話方塊和狀態列上顯示錯誤訊息，提供預設錯誤處理。 您也可以藉由處理腳本中的錯誤，提供自訂錯誤處理。 錯誤處理是事件驅動的，這表示您會收到每個錯誤的通知，且必須決定每個錯誤事件發生時如何處理。 如需使用6.4 版物件模型處理錯誤的詳細資訊，請參閱《 6.4 Player 物件模型指南》的「錯誤處理」一節，這是 Windows Media Player SDK 的一部分。

Windows Media Player 7 或更新版本的物件模型會提供 **Error** 物件和 **ErrorItem** 物件來處理錯誤。 這兩個物件會一起運作，以提供錯誤處理機制，讓您能夠完整且彈性地控制錯誤處理常式。 **Error** 物件提供 **ErrorItem** 物件集合的存取權;每個 **ErrorItem** 物件都會提供個別錯誤訊息的詳細資料。

發生錯誤時，錯誤資訊會張貼到錯誤佇列。 佇列是 **ErrorItem** 物件的集合。 當每個錯誤新增至佇列時，它會與索引編號相關聯， (從) 零開始，可以用來識別特定的 **ErrorItem** 物件。 *錯誤*。**errorCount** 屬性會捕獲錯誤佇列中的錯誤數目。 因為索引編號是以零為起始，所以張貼至佇列的最新錯誤一律會有等於 *錯誤* 的索引值。**errorCount** 減一。

您可以使用腳本來建立 Windows Media Player 的錯誤事件處理常式。 下列 JScript 範例示範如何從錯誤佇列中取出最新的錯誤專案，並使用 Windows Media Player 7 或更新版本的物件模型來顯示錯誤碼和錯誤描述。 使用 ID = "WMP9" 建立 **Player** 物件。


```C++
<!-- Create an error event handler for Windows Media Player 7 or later errors. -->
<SCRIPT  LANGUAGE = "JScript"  FOR = WMP9  EVENT = error()>

// Store the number of errors in the error queue.
var max = WMP9.error.errorCount;

// Retrieve most recent ErrorItem object.
var err = WMP9.error.item(max-1)

// Store the error code number.
var errNum = err.errorCode;

// Store the error description string.
var errDesc = err.errorDescription;

// Build a message string to notify the user.
var msg = "Error number: " + errNum + "\n";
msg += "Error description: " + errDesc;

// Display the message box.
alert(msg);

</SCRIPT>

```



**錯誤** 物件有兩種可供您使用的額外方法。 *錯誤*。**clearErrorQueue** 方法可讓您從錯誤佇列中移除所有錯誤，並將索引編號重設為零。 您可以完全掌控此程式;您可以將錯誤保留在佇列中，只要您需要它們才能使用，然後在完成處理錯誤時清空佇列。

*錯誤*。**webHelp** 方法提供一種方式，可使用網際網路向使用者顯示最新的錯誤資訊。 當呼叫時，這個方法會傳送佇列中第一個錯誤的所有相關資訊， (索引為零) 至 Microsoft Windows Media Player Web 說明，這會在目前的瀏覽器視窗中顯示錯誤的進一步資訊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Error 物件**](error-object.md)
</dt> <dt>

[**ErrorItem 物件**](erroritem-object.md)
</dt> <dt>

[**物件模型遷移指南**](object-model-migration-guide.md)
</dt> </dl>

 

 




