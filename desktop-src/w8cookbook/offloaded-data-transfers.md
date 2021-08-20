---
title: 卸載資料傳輸
description: 卸載資料傳輸
ms.assetid: 91EBE6D6-2DA7-48DA-AEB7-3FAFCA8341F5
keywords:
- odx
- 複製卸載
- 卸載
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7a7e8fc5f360cb1781d4e9aaf84bb206e3facd3787812fb6cc80d9f855d725d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117671958"
---
# <a name="offloaded-data-transfers"></a>卸載資料傳輸

## <a name="platforms"></a>平台

**用戶端**– Windows 8  
**伺服器**– Windows Server 2012  


## <a name="description"></a>描述

為了推進儲存體資料的移動，Microsoft 開發了一項新的資料傳輸技術– (ODX) 卸載資料傳輸。 Windows ODX 不會使用緩衝的讀取和緩衝寫入作業，而是會啟動複製作業，並讀取並取出代表儲存體裝置資料的權杖，然後使用具有權杖的卸載寫入命令來要求從源磁片到目的地磁片的資料移動。 儲存體裝置的複製管理員會根據權杖來執行資料移動。 在 Windows 8 中，IT 管理員和存放裝置系統管理員可以使用 Windows ODX 功能與存放裝置互動，以透過高速儲存網路移動大型檔案或資料。 WindowsODX 會大幅減少大量資料傳輸期間的用戶端伺服器網路流量和 CPU 時間使用量，因為所有資料移動都是在後端儲存體網路上。 ODX 可用於虛擬機器部署、大規模資料移轉和階層式存放裝置的支援，並可透過 ODX 和精簡布建儲存體功能，降低實體硬體部署的成本。

> [!Note]  
> 這項功能只適用于具有 SPC4 和 SBC3 規格執行的儲存裝置。

 

## <a name="functional-details"></a>功能詳細資料

-   Windows ODX 功能內嵌于 Windows 作業系統的複製引擎;在儲存體列舉期間，Windows 將會查詢儲存體裝置的 ODX 功能
-   複製來源儲存體裝置和複製目的地儲存體裝置應在相同的複本管理員下管理，以提供複製卸載支援
-   如果複製卸載作業失敗，儲存裝置的複製管理員必須針對應用程式的錯誤處理傳回適當的額外意義資料
-   如果複製卸載作業失敗，則 Windows 複製引擎會切換回傳統的複製操作

## <a name="using-odx"></a>使用 ODX

-   資料傳輸應用程式必須確保複製來源 LUN 和複製目的地 LUN 都能 ODX，然後再呼叫 ODX API 常式
-   在 Windows explorer 中，使用者可以使用「拖曳」或「複製並貼上」來執行複製卸載
-   當來源 LUN 和目的地 LUN 掛接于檔案系統時，應用程式必須只呼叫 FSCTL 卸載 \_ \_ READ 和 FSCTL 卸載 \_ 寫入， \_ 才能執行從源 lun 到目的地 lun 的資料傳輸
-   如果複製卸載作業失敗，儲存裝置的複製管理員必須針對應用程式的錯誤處理傳回適當的額外意義資料
-   當來源 LUN 或目的地 LUN 未與檔案系統一起裝載且已鎖定時，應用程式必須呼叫 IOCTL \_ 儲存體，並 \_ \_ \_ \_ 使用 DeviceDsmAction \_ OffloadRead 或 DeviceDsmAction OffloadWrite 動作來管理資料集屬性， \_ 以執行複製卸載
-   儲存體管理應用程式可能會 \_ \_ 在來源與目的地 lun 都未與任何檔案系統一起掛接且遭到鎖定時，使用 SCSI PASS 通過 API 來執行卸載資料傳輸

## <a name="tests"></a>測試

-   為確保健全的使用者體驗，請確認存放裝置陣列的 Windows ODX 認證
-   存放裝置必須符合 Windows 卸載資料傳輸認證 (用來作為支援 ODX 功能的標誌) 需求
-   使用 Windows 卸載資料傳輸硬體認證套件來確認存放裝置的 ODX 功能支援

## <a name="resources"></a>資源

-   T10 XCOPY Lite 規格 (11-059r8) 
    -   [https://www.t10.org/cgi-bin/ac.pl?t=f&f=spc4r35b.pdf](https://www.t10.org/cgi-bin/ac.pl?t=f&f=spc4r35b.pdf)
    -   [https://www.t10.org/cgi-bin/ac.pl?t=f&f=sbc3r30.pdf](https://www.t10.org/cgi-bin/ac.pl?t=f&f=sbc3r30.pdf)
-   [硬體儀表板服務](/windows-hardware/drivers/dashboard/)
-   [SCSI \_ \_ 通過結構](/windows-hardware/drivers/ddi/ntddscsi/ns-ntddscsi-_scsi_pass_through)

 

 