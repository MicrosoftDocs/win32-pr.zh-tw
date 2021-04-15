---
description: 搭配磁片配額使用的介面。
ms.assetid: 422d93d9-f4aa-428d-94c1-fdf2dcf4c974
title: 磁片配額介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bbcd4240a6a5910942aad71c7ea080da40918a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104469397"
---
# <a name="disk-quota-interfaces"></a>磁片配額介面

下列介面適用于磁片配額。



| 介面                                          | 描述                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**IDiskQuotaControl**](/windows/win32/api/dskquota/nn-dskquota-idiskquotacontrol)     | 控制單一 NTFS 檔案系統磁片區的磁片配額工具。<br/>                             |
| [**IDiskQuotaEvents**](/windows/win32/api/dskquota/nn-dskquota-idiskquotaevents)       | 接收與配額相關的事件通知。<br/>                                                         |
| [**IDiskQuotaUser**](/windows/win32/api/dskquota/nn-dskquota-idiskquotauser)           | 代表磁片區配額資訊檔案中的單一使用者配額專案。<br/>                          |
| [**IDiskQuotaUserBatch**](/windows/win32/api/dskquota/nn-dskquota-idiskquotauserbatch) | 新增多個配額使用者物件到容器，然後在單一呼叫中提交以進行更新。<br/> |
| [**IEnumDiskQuotaUsers**](/windows/win32/api/dskquota/nn-dskquota-ienumdiskquotausers) | 列舉磁片區上的使用者配額專案。<br/>                                                        |



 

 

