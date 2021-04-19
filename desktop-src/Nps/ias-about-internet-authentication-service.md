---
title: 關於 NPS 擴充功能
description: 本節說明如何執行 Dll 以擴充 NPS 的功能。 它描述 NPS 和 Dll 之間的互動，並提供有關 Dll 的一些設計考慮。
ms.assetid: 3d4d8d22-4cd3-48e0-b4a4-dfa0a0b7b87f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05878a5243774046c1ca052052d59be9378483d6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106994964"
---
# <a name="about-nps-extensions"></a>關於 NPS 擴充功能

> [!Note]  
> 從 Windows Server 2008 開始， (IAS) 的網際網路驗證服務已重新命名為網路原則伺服器 (NPS) 。 本主題的內容適用于 IAS 和 NPS。 在整個文字中，NPS 是用來參考服務的所有版本，包括原本稱為 IAS 的版本。

 

本節說明如何執行 Dll 以擴充 NPS 的功能。 它描述 NPS 和 Dll 之間的互動，並提供有關 Dll 的一些設計考慮。

NPS 提供兩個擴充點，一個用於驗證，另一個用於授權。 驗證是指驗證使用者的身分識別。 授權是指決定網路應提供給使用者的服務。 這兩個擴充點對應于驗證延伸模組 Dll 和授權延伸 Dll。 每個擴充點都可以支援多個 Dll。

NPS 提供驗證和授權服務。 NPS 會在內建 NPS 驗證和授權之前呼叫驗證延伸模組 Dll。 在 NPS 驗證和授權之後，會呼叫授權延伸 Dll。

下圖說明使用擴充 Dll 擴充的 NPS RADIUS 伺服器的封包流程。

![nps 驗證與授權程式](images/ias03.png)

如果驗證延伸模組 DLL 傳回 ACCEPT，封包會略過 NPS 驗證並直接前往 NPS 授權。

> [!Note]  
> 當有多個驗證延伸模組 Dll 時，也會略過其餘的延伸模組 Dll。 如需詳細資訊，請參閱 [設定擴充 dll](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls) 。

 

如果驗證延伸模組 DLL 傳回 CONTINUE，封包會前往 NPS 驗證，然後傳送到 NPS 授權。

> [!Note]  
> 當有多個驗證延伸模組 Dll 時，會在 NPS 驗證之前叫用其餘的驗證延伸模組 Dll。

 

下列主題會更詳細地說明擴充 Dll：

-   [設定延伸模組 Dll](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)
-   [叫用擴充 Dll](/windows/desktop/Nps/ias-authentication-and-authorization-process)
-   [使用者識別屬性](/windows/desktop/Nps/ias-user-identification-attributes)

 

 