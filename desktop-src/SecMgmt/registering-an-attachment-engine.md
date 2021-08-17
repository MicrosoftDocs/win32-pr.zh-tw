---
description: 在安全性設定引擎可以呼叫您的附件引擎來處理服務特定工作之前，您必須先安裝附件引擎，並向安全性設定引擎註冊。
ms.assetid: f7376a79-97cd-4607-9e1b-5b8c7cd76a32
title: 註冊附件引擎
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04d3d13bab6c26254295734344011a9f56457b8fac28c913178c7515cc147fb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118893697"
---
# <a name="registering-an-attachment-engine"></a>註冊附件引擎

在安全性設定引擎可以呼叫您的附件引擎來處理服務特定工作之前，您必須先安裝附件引擎，並向安全性設定引擎註冊。

**安裝並註冊附件引擎 DLL**

1.  將附件引擎 DLL 複製到系統上的目錄。 慣用的目錄為% windir% \\ secedit 個 \\ 附件。 如果此目錄不存在，您應該建立它。
2.  在下列節點底下建立登錄機碼。 *服務名稱* 是附件的註冊名稱，而且必須是服務控制管理員中所使用的相同服務名稱，也就是管理服務停止和啟動的模組。 名稱也必須是唯一的，因此它不會與其他附件的名稱衝突。

    ```
    HKEY_LOCAL_MACHINE
       Microsoft
          Windows NT
             CurrentVersion
                SeCEdit
                   Service
                      service name
    ```

3.  在新的登錄機碼中建立下列字串值。 *附件引擎路徑* 是附件引擎模組的完整路徑。<dl> <dd>**ServiceAttachmentPath**  = *附件引擎路徑*<dl> <dt>

資料類型
</dt> <dd>REG_SZ</dd> </dl> </dd> </dl>

 

 



