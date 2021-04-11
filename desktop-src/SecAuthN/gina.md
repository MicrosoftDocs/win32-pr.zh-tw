---
description: GINA DLL 的目的是要提供可自訂的使用者識別和驗證程式。 預設 GINA 會藉由將 SAS 事件監視委派給 Winlogon 來執行此工作，以接收和處理 CTL + ALT + DEL 安全的注意順序 (SASs) 。
ms.assetid: 035e9c8b-2490-438d-8f02-7e0f039f960f
title: 吉娜
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 084a65ad42bdbe030e697481501a4dc60e54baef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694152"
---
# <a name="gina"></a>吉娜

[*GINA*](/windows/desktop/SecGloss/g-gly)會在 [*Winlogon*](/windows/desktop/SecGloss/w-gly)進程的 [*內容*](/windows/desktop/SecGloss/c-gly)中運作，因此，GINA DLL 在開機過程中會提早載入。 GINA DLL 必須遵循規則，才能維持系統的完整性（特別是與使用者互動的相關）。

> [!Note]  
> 在 Windows Vista 中會忽略 GINA Dll。

 

GINA 最常見的用途是與外部裝置（例如智慧卡 [*讀卡機*](/windows/desktop/SecGloss/r-gly)）通訊。 您必須將設備磁碟機的 start 參數設定為 system (Winnt： SERVICE \_ system \_ start) ，以確保驅動程式是在叫用 GINA 時載入的。

GINA DLL 的目的是要提供可自訂的使用者識別和驗證程式。 預設 GINA 會藉由將 SAS 事件監視委派給 Winlogon 來執行此工作，以接收和處理 CTL + ALT + DEL [*安全的注意順序*](/windows/desktop/SecGloss/s-gly) (SASs) 。 自訂 GINA 會負責將本身設定為接收 SAS 事件 (除了預設的 CTRL + ALT + DEL SAS 事件) 之外，還會在 SAS 事件發生時通知 Winlogon。 Winlogon 會評估其狀態，以判斷處理自訂 GINA SAS 所需的內容。 這種處理通常包含對 GINA SAS 處理函式的呼叫。

如需特定 GINA 匯出函數的詳細資訊，請參閱 [GINA 匯出](authentication-functions.md)函式。 如需使用 GINA 結構傳遞資訊的相關資訊，請參閱 [GINA 結構](authentication-structures.md)。



| 主題                                                                             | 描述                                                                     |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [載入和執行 GINA DLL](loading-and-running-a-gina-dll.md)<br/>   | 要改變以載入和執行自訂 GINA DLL 的登錄機碼值。<br/> |
| [建立和測試 GINA DLL](building-and-testing-a-gina-dll.md)<br/> | 如何測試 GINA DLL。<br/>                                              |



 

 

