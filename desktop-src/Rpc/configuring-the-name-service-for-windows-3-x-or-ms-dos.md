---
title: 設定 Windows 3.x 或 MS-DOS 的名稱服務
description: 遠端程序呼叫 (RPC) ，並設定 Windows 3.x 或 MS-DOS 的名稱服務。
ms.assetid: 7b22a12e-43d0-4e32-a191-d63a56559143
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24884c782913c47806c702ff129594c6524fe7c0e731561de405f3b6a360c7c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022428"
---
# <a name="configuring-the-name-service-for-windows-3x-or-ms-dos"></a>設定 Windows 3.x 或 MS-DOS 的名稱服務

當您執行 Setup.exe 安裝16位的 RPC 執行時間程式庫時，它會提示您選取名稱服務提供者：

-   如果您選擇 [ **安裝預設名稱服務提供者**]，則會安裝預設的 NSP （Microsoft 定位器）。
-   如果您選擇 [ **安裝自訂名稱服務提供者**]，請完成 [ **定義網路位址** ] 對話方塊，將 [DCE Cell Directory 服務安裝為您的 NSP。 DCE Cell Directory 服務是與 DCE 伺服器搭配使用的 NSP。

網路位址是執行 NSI daemon (nsid) 的主電腦名稱稱。 此電腦可作為 DCE Cell Directory 服務的閘道，並在執行 Microsoft 作業系統和 DCE 電腦的電腦之間傳遞 NSI 函數呼叫。 網路位址可以是80個字元或更少，例如，11.1.9.169 是有效的位址。

 

 




