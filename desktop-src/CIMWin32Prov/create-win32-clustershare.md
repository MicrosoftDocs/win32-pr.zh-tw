---
description: 建立新的 Win32 \_ ClusterShare 實例。
ms.assetid: a6fde28d-f19e-4a31-8f0d-35927c75a030
ms.tgt_platform: multiple
title: Win32_ClusterShare 類別的 Create 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: edaafa00f792cf01b4166d525171cf15b7f781c8c0c943c17377b3bd9b3401dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119020586"
---
# <a name="create-method-of-the-win32_clustershare-class"></a>Win32 ClusterShare 類別的 Create 方法 \_

建立新的 [**Win32 \_ ClusterShare**](win32-clustershare.md) 實例。

## <a name="syntax"></a>語法


```mof
static uint32 Create(
  [in]           string                   Path,
  [in]           string                   Name,
  [in]           uint32                   Type,
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] string                   Password,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*路徑* \[在\]
</dt> <dd>

Windows 共用的本機路徑。

範例： "C： \\ Program Files"。

</dd> <dt>

*名稱* \[在\]
</dt> <dd>

在執行 Windows 的電腦系統上，設定為共用的路徑別名。

範例： "public"。

</dd> <dt>

*類型* \[在\]
</dt> <dd>

共用的資源類型。 類型包括：磁片磁碟機、列印佇列、處理序間通訊 (IPC) 和一般裝置。

<dt>

0 (0x0) 
</dt> <dd>

磁碟機

</dd> <dt>

1 (0x1) 
</dt> <dd>

列印佇列

</dd> <dt>

2 (0x2) 
</dt> <dd>

裝置

</dd> <dt>

3 (0x3) 
</dt> <dd>

IPC

</dd> <dt>

2147483648 (0x80000000) 
</dt> <dd>

磁片磁碟機系統管理員

</dd> <dt>

2147483649 (0x80000001) 
</dt> <dd>

列印佇列管理員

</dd> <dt>

2147483650 (0x80000002) 
</dt> <dd>

裝置系統管理員

</dd> <dt>

2147483651 (0x80000003) 
</dt> <dd>

IPC 系統管理員

</dd> </dl> </dd> <dt>

*MaximumAllowed* \[在中，選擇性\]
</dt> <dd>

允許同時使用此資源的使用者數目上限。

</dd> <dt>

*描述* \[在中，選擇性\]
</dt> <dd>

物件的描述。

</dd> <dt>

*密碼* \[在中，選擇性\]
</dt> <dd>

TBD

</dd> <dt>

*存取* \[在中，選擇性\]
</dt> <dd>

[**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)類別的選擇性內嵌實例，其中包含新共用的安全描述項。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7<br/>                                                                    |
| 最低支援的伺服器<br/> | Windows Server 2008 R2<br/>                                                       |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ ClusterShare**](win32-clustershare.md)
</dt> </dl>

 

