---
description: .
ms.assetid: 0ea1de35-34ea-4e94-b90d-0f89503cb3fb
title: 動態記憶體
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a1e868a89714a7f6f1d77f9416515897876c150
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988441"
---
# <a name="dynamic-memory"></a>動態記憶體

## <a name="affected-platforms"></a>受影響的平臺

**用戶端 () 的虛擬機器** 執行-windows Vista \| windows 7  
**伺服器** -Windows Server 2008 R2 hyper-v SP1  


## <a name="feature-impact"></a>功能影響

 **嚴重性** -低  
**頻率** -高  






## <a name="description"></a>Description

概括而言，Hyper-v 動態記憶體是 Windows Server 2008 R2 SP1 內含之 Hyper-v 角色的記憶體管理增強功能。 它是專為生產環境使用而設計，可讓客戶達到更高的匯總/虛擬機器 (VM) 密度比例，同時優化實體機器中的記憶體使用率。 系統會減少靜態記憶體配置，並視需要配置額外的記憶體。 動態記憶體會影響需要確保其軟體在虛擬機器環境中正常運作的軟體發展人員。

## <a name="usage-scenario"></a>使用案例

有兩個主要的使用案例，其中動態記憶體進入 play、主機端應用程式和來賓端應用程式。

**主機端應用程式 (管理工具)**

管理新的 Windows Server 2008 R2 SP1 伺服器的舊版工具將無法存取新的動態記憶體設定。 已開發新的 WMI Api 和效能計數器，以管理 Hyper-v 虛擬機器的新動態記憶體設定。 處理管理工具的軟體發展人員應該利用這些 Api 和計數器，以搭配已安裝 Hyper-v 角色的 Windows Server 2008 R2 SP1 使用。 有關這些新 Api 的詳細資料，可透過 [MSDN 上的 HYPER-V WMI 提供者檔](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider)取得。

**來賓端應用程式**

撰寫要在設定為使用動態記憶體的虛擬機器中使用的軟體的開發人員必須記住，VM 系統記憶體不再是固定的。 因此，其應用程式應該在不再需要時釋放記憶體，讓其他應用程式能夠利用資源。

在使用者應用程式中，記憶體配置和取消配置仍會持續正常運作。 動態記憶體對大部分的終端使用者應用程式而言都是完全透明的。 但是，如果所開發的軟體會使用虛擬機器中的記憶體效能計數器，則應該在啟用動態記憶體的環境中執行測試，以確保軟體會將對客體作業系統記憶體配置所做的變更納入考慮。 從虛擬機器的觀點來看，可用記憶體不再是「靜態」。

## <a name="solutions"></a>方案

虛擬機器必須安裝更新的 integration services (SP1) ，才能利用動態記憶體。 確定 Hyper-v 虛擬機器管理中使用的所有電腦都使用最新的 Windows Server 2008 R2 SP1 位。

## <a name="links-to-other-resources"></a>其他資源的連結

-   [動態記憶體進入 Hyper-v 的 blog](https://blogs.technet.com/b/virtualization/archive/2010/03/18/dynamic-memory-coming-to-hyper-v.aspx)
-   [使用 Hyper-v WMI 提供者](/previous-versions/windows/desktop/virtual/using-the-virtualization-wmi-provider)

## <a name="disclaimer"></a>免責聲明

本檔中包含的資訊與搶鮮版軟體產品相關，該產品可能會在其第一個商業發行之前經過大幅修改。 因此，在第一次正式發行時，資訊可能無法正確描述或反映軟體產品。 此文件僅供參考之用。 MICROSOFT MAKES NO WARRANTIES, EXPRESS OR IMPLIED, IN THIS DOCUMENT.

 

 
