---
title: 核心模式驅動程式的安全開機功能簽署需求
description: 核心模式驅動程式的安全開機功能簽署需求
ms.assetid: 7FF64BA2-89E3-4E6F-B542-7BC7BF7F4FB2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a63a8b1fca1677aa125bac96dfec290dcd736b5
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "106993736"
---
# <a name="secure-boot-feature-signing-requirements-for-kernel-mode-drivers"></a>核心模式驅動程式的安全開機功能簽署需求

## <a name="platforms"></a>平台

**用戶端** – Windows 8  
**伺服器** – Windows Server 2012  


## <a name="description"></a>Description

在 Windows 8 和 Windows Server 2012 （包括 WinPE）中，核心已被鎖定，以防止開機或根套件所引進的惡意程式碼規避簽署驅動程式的 Windows 作業系統安全性需求。

此變更會影響支援整合可延伸韌體介面之裝置的所有核心模式驅動程式 (UEFI) 安全開機;Windows 8 用戶端電腦的認證，以及伺服器的選擇性選項，都需要 UEFI 安全開機。 它不會影響使用者模式驅動程式。

核心模式驅動程式的標準開發牽涉到使用核心模式的偵錯工具或開機設定資料 (BCD) <testsigning> 設定。 開啟安全開機時，這兩個都是停用的。

## <a name="manifestation"></a>表現

如果不是由受信任的憑證授權單位單位 (CA) 正確簽署，就不會執行核心模式驅動程式。 作業系統將不會允許不受信任的驅動程式執行，而且不允許使用標準機制，例如內核偵錯工具和 testsigning。

## <a name="mitigation"></a>降低

若要測試驅動程式，您必須停用 BIOS 中的安全開機，並符合其他測試簽署需求 (請參閱以下) 。

更廣泛地散發驅動程式時，必須由受信任的 CA 正確簽署。

## <a name="resources"></a>資源

-   [簽署驅動程式](/previous-versions/windows/hardware/design/dn653563(v=vs.85))

 

 