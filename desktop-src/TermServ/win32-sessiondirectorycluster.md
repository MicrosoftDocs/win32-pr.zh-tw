---
title: Win32_SessionDirectoryCluster 類別
description: 提供屬性，以在遠端桌面連線代理人 (RD 連線代理人) 中查看伺服器陣列的屬性。
ms.assetid: a4a924fd-88ea-46db-968e-378c3dc46cfc
ms.tgt_platform: multiple
keywords:
- Win32_SessionDirectoryCluster 類別遠端桌面服務
- Win32_SessionDirectoryCluster 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryCluster
- Win32_SessionDirectoryCluster.ClusterName
- Win32_SessionDirectoryCluster.NumberOfServers
- Win32_SessionDirectoryCluster.SingleSessionMode
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f1dba262ddb332f03c7f398c4f205e73a9c9e94054d4164fb94c8c01dc8b505
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127078"
---
# <a name="win32_sessiondirectorycluster-class"></a>Win32 \_ SessionDirectoryCluster 類別

提供屬性，以在遠端桌面連線代理人 (RD 連線代理人) 中查看伺服器陣列的屬性。

> [!Note]  
> 在 Windows Server 2008 R2 中，終端機服務會話代理人 (TS 會話代理人) 的名稱已變更為 RD 連線代理人。 除非另有說明，否則這些屬性適用于所有支援的作業系統。

 

## <a name="syntax"></a>語法

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYCLUSTER_Prov"), AMENDMENT]
class Win32_SessionDirectoryCluster
{
  string ClusterName;
  uint32 NumberOfServers;
  uint32 SingleSessionMode;
};
```

## <a name="members"></a>成員

**Win32 \_ SessionDirectoryCluster** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ SessionDirectoryCluster** 類別具有這些屬性。

<dl> <dt>

**ClusterName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

RD 連線代理人中伺服器陣列的名稱。

</dd> <dt>

**NumberOfServers**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

RD 連線代理人中伺服器陣列中的伺服器數目。

</dd> <dt>

**SingleSessionMode**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

RD 連線代理人中伺服器陣列的單一會話模式。

<dt>

0
</dt> <dd>

RD 連線代理人中的伺服器陣列不在單一會話模式中。

</dd> <dt>

1
</dt> <dd>

RD 連線代理人中的伺服器陣列處於單一會話模式。

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>備註

受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。 MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。 當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。 如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                         |
| 命名空間<br/>                | Root\\CIMv2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>TssdWmi mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ SessionDirectoryServer**](win32-sessiondirectoryserver.md)
</dt> <dt>

[**Win32 \_ SessionDirectorySession**](win32-sessiondirectorysession.md)
</dt> </dl>

 

