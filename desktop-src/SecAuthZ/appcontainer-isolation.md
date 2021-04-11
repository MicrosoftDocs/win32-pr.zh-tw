---
description: 隔離是 AppContainer 執行環境的主要目標。
ms.assetid: 13C579F9-7F9F-4602-9B03-08CD820C3BBA
title: AppContainer 隔離
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82fec44fd3d6eb9495370c42e52726ceb0f63806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194057"
---
# <a name="appcontainer-isolation"></a>AppContainer 隔離

隔離是 AppContainer 執行環境的主要目標。 藉由將應用程式與不需要的資源和其他應用程式隔離，可將惡意操作的機會降到最低。 根據最低許可權授與存取權，可防止應用程式和使用者存取其權利以外的資源。 控制資源的存取可保護進程、裝置和網路。

Windows 中的大部分弱點都是從應用程式開始。 一些常見的範例包括從其瀏覽器中斷的應用程式，或是將錯誤檔傳送至 Internet Explorer 以及利用外掛程式（例如 flash）。 這些應用程式可以在 AppContainer 中隔離，而裝置和資源就越安全。 即使應用程式中的弱點遭到惡意探索，應用程式仍無法存取授與 AppContainer 以外的資源。 惡意應用程式無法接管電腦的其餘部分。

## <a name="credential-isolation"></a>認證隔離

若要管理身分識別和認證，AppContainer 會防止使用使用者認證來存取資源或登入其他環境。 AppContainer 環境會建立識別碼，其利用使用者和應用程式的組合身分識別，因此認證對每個使用者/應用程式配對而言都是唯一的，且應用程式無法模擬使用者。

## <a name="device-isolation"></a>裝置隔離

將應用程式與裝置資源隔離，例如被動式感應器 (攝影機、麥克風、GPS) 和貨幣泵 (3G/4G、撥打電話) AppContainer 環境會防止應用程式惡意利用裝置。 依預設會封鎖這些資源，並且可以視需要授與存取權。 在某些情況下，這些資源會由「訊息代理程式」進一步保護。 有些資源（例如鍵盤和滑鼠）一律可供 AppContainer 和常駐應用程式使用。

## <a name="file-isolation"></a>檔案隔離

控制檔案和登錄存取，AppContainer 環境可防止應用程式修改不應使用的檔案。 可將讀寫存取權授與特定的持續性檔案和登錄機碼。 唯讀存取的限制較少。 應用程式一律可以存取專為該 AppContainer 建立的記憶體常駐檔案。

## <a name="network-isolation"></a>網路隔離

除了特別配置的網路資源之外，AppContainer 還可防止應用程式「將其環境「進行」「進行」，並惡意地利用網路資源。 您可以授與存取網際網路、內部網路存取，以及做為伺服器的細微存取權。

## <a name="process-isolation"></a>處理序隔離

將應用程式核心物件沙箱化，AppContainer 環境可防止應用程式影響或受到其他應用程式進程的影響。 這可防止適當包含的應用程式在發生例外狀況時損毀其他進程。

## <a name="window-isolation"></a>視窗隔離

將應用程式與其他視窗隔離，AppContainer 環境可防止應用程式影響其他應用程式介面。

 

 



