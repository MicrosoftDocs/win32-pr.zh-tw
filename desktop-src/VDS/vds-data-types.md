---
description: VDS 所支援的資料類型會定義函數傳回值、函數參數和結構成員。 資料類型會定義這些元素的大小和意義。
ms.assetid: f17e8c7e-e3cb-49ca-9060-2299dda55770
title: VDS 資料類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a868606110d9cf1c3cad5c3036789d041a5d86c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985355"
---
# <a name="vds-data-types"></a>VDS 資料類型

\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]

VDS 所支援的資料類型會定義函數傳回值、函數參數和結構成員。 資料類型會定義這些元素的大小和意義。



| 資料類型                                                                                      | 描述                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VDS_OBJECT_ID"></span><span id="vds_object_id"></span>**VDS \_ 物件 \_ 識別碼**<br/> | VDS 物件識別碼。 在重新開機時，這些值不保證是唯一的。 <br/> 這種類型是在 Vds. h (VdsHwPrv，) 硬體提供者的 GUID。 <br/> |
| <span id="VDS_PATH_ID"></span><span id="vds_path_id"></span>**VDS \_ 路徑 \_ 識別碼**<br/>       | 多重路徑 i/o (MPIO) 的 VDS 路徑識別碼。 <br/> 這種類型是在 Vds. h (VdsHwPrv，) 作為 UINT64 的硬體提供者。<br/>                                      |



 

 

