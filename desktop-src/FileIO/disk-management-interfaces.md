---
description: 磁片管理中使用的介面。
ms.assetid: c1f79e2e-834b-41dc-a15f-6dd1034d021b
title: 磁片管理介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c86881ff3bf6232da68c4cf1539dbbedf87c50f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194400"
---
# <a name="disk-management-interfaces"></a>磁片管理介面

下列介面用於磁片管理。

## <a name="in-this-section"></a>本節內容



| 介面                                                     | 描述                                                                                                    |
|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**IDiskQuotaControl**](/windows/win32/api/dskquota/nn-dskquota-idiskquotacontrol)<br/>     | 控制單一 NTFS 檔案系統磁片區的磁片配額工具。<br/>                             |
| [**IDiskQuotaEvents**](/windows/win32/api/dskquota/nn-dskquota-idiskquotaevents)<br/>       | 接收與配額相關的事件通知。<br/>                                                         |
| [**IDiskQuotaUser**](/windows/win32/api/dskquota/nn-dskquota-idiskquotauser)<br/>           | 代表磁片區配額資訊檔案中的單一使用者配額專案。<br/>                          |
| [**IDiskQuotaUserBatch**](/windows/win32/api/dskquota/nn-dskquota-idiskquotauserbatch)<br/> | 新增多個配額使用者物件到容器，然後在單一呼叫中提交以進行更新。<br/> |
| [**IEnumDiskQuotaUsers**](/windows/win32/api/dskquota/nn-dskquota-ienumdiskquotausers)<br/> | 列舉磁片區上的使用者配額專案。<br/>                                                        |



 

 

