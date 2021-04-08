---
description: 成功認可佇列之後，您將需要更新您要安裝之產品的登錄資訊。
ms.assetid: 32161538-c1bd-41a0-bb4f-a32883fe8285
title: 更新登錄資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aa6a77f231f3a4fe754b589e3f20ed67e78e548
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944937"
---
# <a name="updating-registry-information"></a>更新登錄資訊

成功認可佇列之後，您將需要更新您要安裝之產品的登錄資訊。 建議您等到所有必要的檔案複製作業順利完成後，再改變登錄資訊。

更新登錄的其中一種方式是呼叫 [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) \_ ，並指定 SPINST INIFILES、SPINST \_ registry 或 SPINST \_ INI2REG 旗標。 您可以在 **SetupInstallFromInfSection** 的單一呼叫中結合這些旗標。

下列範例會使用 SPINST \_ ALL ^ SPINST 檔案 \_ 來表示函式應處理所有列出的作業（檔案作業除外）。 由於只有 INI、登錄和檔案作業會列在 [ **安裝** ] 區段中，因此這是指定函式應處理所有 INI 和登錄作業的速記方法。

下列範例示範如何使用 **SetupInstallFromINFSection** 函式來安裝登錄資訊。

``` syntax
Test = SetupInstallFromINFSection (
     NULL,                     //Window to own any dialog boxes
                               //created 
     MyInf,                    //INF file containing the section 
     MySection,                //the section to install
     SPINST_ALL ^ SPINST_FILES,//which installation operations 
                               //to process
     NULL,                     //the relative root key
     NULL,                     //the source root path
     0,                        //copy style
     NULL,                     //Message handler routine
     NULL,                     //Context
     NULL,                     //Device info set
     NULL                      //device info data
);
```

在此範例中， *OwnerWindow* 是 **Null** ，因為只有檔案作業會產生對話方塊，因此不需要父視窗。 "MyInf" 是包含要處理之區段的 INF 檔案。 參數 "MySection" 指定要安裝的區段。 組合旗標 SPINST \_ 所有 ^ SPINST 檔案 \_ ，指定要處理的安裝作業，在此案例中為檔案作業以外的所有作業。 來源根路徑指定為 "A： \\ "。

因為未處理任何複製作業，所以未指定 *CopyFlags*、 *MsgHandler*、 *CoNtext*、 *DeviceInfoSet* 和 *DeviceInfoData* 參數。

 

 



