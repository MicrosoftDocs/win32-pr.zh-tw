---
description: 代表磁碟分割管理員上針對屬於叢集一部分之磁片所維護的資訊。
ms.assetid: 9138F61A-E295-4F5B-AD65-361FCCB3C4B7
title: 'DISK_CLUSTER_INFO 結構 (Ntdddisk .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DISK_CLUSTER_INFO
api_type:
- HeaderDef
api_location:
- Ntdddisk.h
ms.openlocfilehash: be4db89e888778c3d92090a32243f0203b527337b3734328a183b551a6181f7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813790"
---
# <a name="disk_cluster_info-structure"></a>磁片 \_ 群集 \_ 資訊結構

代表磁碟分割管理員上針對屬於叢集一部分之磁片所維護的資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _DISK_CLUSTER_INFO {
  ULONG     Version;
  ULONGLONG Flags;
  ULONGLONG FlagsMask;
  BOOLEAN   Notify;
} DISK_CLUSTER_INFO, *PDISK_CLUSTER_INFO;
```



## <a name="members"></a>成員

<dl> <dt>

**版本**
</dt> <dd>

版本號碼。 此值必須設定為此結構的大小。

</dd> <dt>

**旗標**
</dt> <dd>

與磁片和叢集相關的旗標組合。



| 值                                                                                                                                                                                                                                                                                               | 意義                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span id="DISK_CLUSTER_FLAG_ENABLED"></span><span id="disk_cluster_flag_enabled"></span><dl> <dt>**磁片 \_叢集 \_ 旗標 \_ 已啟用**</dt> <dt>1</dt> </dl>                                          | 磁片會當做叢集服務的一部分使用。<br/>                                                             |
| <span id="DISK_CLUSTER_FLAG_CSV"></span><span id="disk_cluster_flag_csv"></span><dl> <dt>**磁片 \_群集 \_ 旗標 \_ CSV**</dt> <dt>2</dt> </dl>                                                      | 磁片上的磁片區是由所有叢集節點上的 CSVFS 所公開。<br/>                                        |
| <span id="DISK_CLUSTER_FLAG_IN_MAINTENANCE"></span><span id="disk_cluster_flag_in_maintenance"></span><dl> <dt>**磁片 \_\_維護 4 \_ 中 \_ 的群集旗**</dt>標 <dt></dt> </dl>                    | 與此磁片相關聯的叢集資源處於維護模式。<br/>                                       |
| <span id="DISK_CLUSTER_FLAG_PNP_ARRIVAL_COMPLETE"></span><span id="disk_cluster_flag_pnp_arrival_complete"></span><dl> <dt>**磁片 \_叢集 \_ 旗標 \_ PNP \_ 抵達 \_ 完成**</dt> <dt>8</dt> </dl> | 適用于核心模式的叢集磁片驅動程式 (clusdisk) 已收到磁片抵達的 PnP 通知。<br/> |



 

</dd> <dt>

**FlagsMask**
</dt> <dd>

**旗** 標成員中正在修改的旗標。

</dd> <dt>

**通知**
</dt> <dd>

**TRUE** 表示傳送配置變更通知;否則 **為 FALSE**。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                             |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Ntdddisk。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[磁片管理結構](disk-management-structures.md)
</dt> <dt>

[**IOCTL \_ 磁片 \_ 取得 \_ 叢集 \_ 資訊**](ioctl-disk-get-cluster-info.md)
</dt> <dt>

[**IOCTL \_ 磁片 \_ 集 \_ 叢集 \_ 資訊**](ioctl-disk-set-cluster-info.md)
</dt> </dl>

 

 




