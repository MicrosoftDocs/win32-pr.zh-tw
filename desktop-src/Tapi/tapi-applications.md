---
description: 下列內容提供使用 TAPI 撰寫終端使用者或伺服器通訊應用程式的指導方針。 這項資訊也與服務提供者程式設計師高度相關。
ms.assetid: fb97aff7-910e-451f-b183-36324a459423
title: TAPI 應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6836f33af120171016b080693ae7a8315f9b9d7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984701"
---
# <a name="tapi-applications"></a>TAPI 應用程式

下列內容提供使用 TAPI 撰寫終端使用者或伺服器通訊應用程式的指導方針。 這項資訊也與服務提供者程式設計師高度相關。

程式設計師需要使用 TAPI 進行的第一個決策是需要的服務層級。 例如，如果應用程式需要可撥電話號碼的功能表選取專案，則可能不需要完整的 TAPI 應用程式。 輔助電話語音可以快速且單純地啟用此選項。 如需完整 TAPI 應用程式和輔助電話語音之間差異的詳細資訊，請參閱 [服務的 TAPI 等級](tapi-levels-of-service.md) 。

第二個重要的決定是要使用 TAPI 2.x、以 C 為基礎的 API，或 TAPI 3.x （以 COM 為基礎）。 請參閱 [tapi 3.x 與 tapi](tapi-3-x-versus-tapi-2-x.md) 2.x，以瞭解決定要使用哪一項的重要考慮。

下圖說明完整 TAPI 應用程式的基本組建區塊。 TAPI 2.x 和 TAPI 3.x 都在這些章節中解決。 在 TAPI 2.x 或 TAPI 3.x 的總覽章節中，將會說明高度特定的材質。

![tapi 應用程式的建立區塊](images/tapior3.png)

下列連結提供的內容對應至上圖中的圖表：

| 圖 | 文件                                                                    |
|--------|----------------------------------------------------------------------------------|
| 1      | [TAPI 初始化](tapi-initialization.md)                                   |
| 2      | [會話控制項](session-control.md)                                           |
| 3      | [裝置控制](device-control.md)                                             |
| 4      | [媒體控制項](media-control.md)                                               |
| 5      | [關於撥置中心控制項](about-call-center-controls.md)                     |
| 6      | [彙集 IP 電話語音會議](rendezvous-ip-telephony-conferencing.md) |
| 7      | [TAPI 關機](tapi-shutdown.md)                                               |



 

 

 



