---
description: 若要讓應用程式使用任何 TAPIs 30 補充電話功能，它需要連線到 TAPI，才能接收訊息。
ms.assetid: c0211f64-4f73-4348-ae49-9a898d3aa093
title: 初始化和關閉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7414b78636a7ce7bf93e297b0cbef4d9dc7d6482191c1b1948235d1dc117423
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867288"
---
# <a name="initialization-and-shutdown"></a>初始化和關閉

若要讓應用程式使用任何 TAPI 的30個補充電話功能，它需要連線到 TAPI，才能接收訊息。 應用程式會使用 [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) 函數來建立此連接。 在此函式中，應用程式會指定通知機制，讓 TAPI 用來通知應用程式的電話狀態變更，以及電話功能的非同步完成。

[**PhoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)函式會將兩項資訊傳回給應用程式：*應用程式控制碼*，以及電話裝置數目。 應用程式控制碼代表應用程式的 TAPI 使用情形。 使用電話控制碼的 TAPI 函式不需要應用程式控制碼，因為此控制碼衍生自指定的電話控點。

[**PhoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)所傳回的第二個資訊是可供 TAPI 使用的電話裝置數目。 電話裝置 (*裝置* 識別碼) 的裝置識別碼來識別。 有效的裝置識別碼範圍從零到電話裝置數目減一。 例如，如果 **phoneInitializeEx** 報告系統中有兩個電話裝置，則有效的電話裝置識別碼為0和1。 使用 TAPI 的電話功能完成應用程式之後，它會叫用 [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)，並傳遞其應用程式控制碼以關閉其使用 tapi。 這可讓 TAPI 釋放指派給應用程式的任何資源。

應用程式不應叫用 [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) ，而不需再開啟電話 (至少用於監視) 。 如果應用程式未監視，且未使用任何裝置，則應該呼叫 [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown) ，以便在不需要時釋放 TAPI 動態連結程式庫所配置的記憶體資源，而且可以在不需要時從記憶體卸載程式庫本身。

[**PhoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)和 [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)都是以同步方式運作。 也就是說，這些函式會傳回成功或失敗指示，而且永遠不會傳回非同步要求識別碼。

 

 



