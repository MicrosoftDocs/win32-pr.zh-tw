---
description: 系統管理員可以控制每位使用者可以儲存在 NTFS 檔案系統磁片區的資料量。
ms.assetid: 42efbd5b-6455-4319-a76e-cdb666fc36b8
title: 管理磁片配額
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5231d7683f0af40e7006193be8d5ff9390e21b65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000178"
---
# <a name="managing-disk-quotas"></a>管理磁片配額

NTFS 檔案系統支援 *磁片配額*，可讓系統管理員控制每位使用者可在 NTFS 檔案系統磁片區上儲存的資料量。 系統管理員可以選擇性地設定系統在使用者接近其配額時記錄事件，以及拒絕超過其配額的使用者更多磁碟空間。 系統管理員也可以產生報表，並使用事件監視器來追蹤配額問題。

您可以藉由呼叫 [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) 函式並檢查檔案 **磁片區 \_ \_ 配額** 位旗標，判斷檔案系統是否支援磁片配額。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                   | 描述                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [磁片配額的使用者層級管理](user-level-administration-of-disk-quotas.md)<br/>     | 如何在超過配額額度之後取得更多可用磁碟空間。<br/>                                                                  |
| [磁片配額的系統層級管理](system-level-administration-of-disk-quotas.md)<br/> | 系統管理員可以設定磁片區上特定使用者的配額。 系統管理員也可以設定磁片區的預設配額。<br/> |
| [磁片配額限制](disk-quota-limits.md)<br/>                                                   | 描述兩種類型的磁片配額限制，以及如何測量磁片配額限制。<br/>                                                      |
| [磁片配額介面](disk-quota-interfaces.md)<br/>                                           | 搭配磁片配額使用的介面。<br/>                                                                                                     |



 

 

 




