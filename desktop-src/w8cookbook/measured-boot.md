---
title: 測量開機
description: 測量開機
ms.assetid: D7ED02FA-6D0F-4753-AC07-BD7DCE55B3FD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d728a1980bc9a461e6383b1dea2bd7eb4aab461
ms.sourcegitcommit: f14de4414da072d5a761e946aedfde24d8b65102
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/30/2021
ms.locfileid: "108314339"
---
# <a name="measured-boot"></a>測量開機

## <a name="platforms"></a>平台

 **客戶** 端-Windows 8  
**伺服器** -Windows Server 2012  



## <a name="description"></a>Description

由於反惡意程式碼 (AM) 軟體在偵測到執行時間惡意程式碼時變得更好且更好，攻擊者也會在建立可隱藏偵測的 rootkit 時變得更好。 偵測開機週期初期啟動的惡意程式碼，是大部分的廠商都能處理的挑戰。 一般情況下，它們會建立主機作業系統不支援的系統駭客，而且實際上會導致電腦處於不穩定的狀態。 到目前為止，Windows 尚未提供良好的方式來偵測並解決這些早期開機的威脅。 Windows 8 引進稱為測量開機的新功能，它會測量每個元件，從透過開機啟動驅動程式的固件，將這些測量儲存在電腦上的信賴平臺模組 (TPM) ，然後提供可從遠端測試以驗證用戶端開機狀態的記錄檔。

## <a name="manifestation"></a>表現

測量開機功能提供受信任 (的軟體，可抵禦軟體之前啟動的所有開機元件的詐騙和篡改) 記錄。 AM 軟體可以使用記錄來判斷在它是否值得信任之前執行的元件，或是否已受到惡意程式碼感染。 本機電腦上的 AM 軟體可以將記錄傳送到遠端伺服器進行評估。 遠端伺服器可能會藉由與用戶端上的軟體互動或依適當的頻外機制來啟動補救動作。

## <a name="mitigation"></a>降低

在企業案例中，系統管理員可以控制測量開機資訊的使用方式。 在使用者案例中（例如，線上銀行) ），取用者必須選擇將測量開機用於特定的服務。

## <a name="solution"></a>解決方法

正在準備白皮書，以詳細說明必須針對各種測量開機案例進行的 Api 和函式呼叫。

 

 




