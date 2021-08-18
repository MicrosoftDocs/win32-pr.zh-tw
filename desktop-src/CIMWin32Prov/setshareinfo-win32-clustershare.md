---
description: 設定共用資源的參數。
ms.assetid: 592d0fa6-c865-4f70-89c3-b58204a8c5a6
ms.tgt_platform: multiple
title: Win32_ClusterShare 類別的 SetShareInfo 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClusterShare.SetShareInfo
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 07245e97e091f607d142de57c00109d3671bd81b5f34b9062681229090ff6b50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119439398"
---
# <a name="setshareinfo-method-of-the-win32_clustershare-class"></a>Win32 ClusterShare 類別的 SetShareInfo 方法 \_

設定共用資源的參數。

## <a name="syntax"></a>語法


```mof
uint32 SetShareInfo(
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*MaximumAllowed* \[在中，選擇性\]
</dt> <dd>

允許同時使用此資源的使用者數目上限。

</dd> <dt>

*描述* \[在中，選擇性\]
</dt> <dd>

描述正在共用的資源。

</dd> <dt>

*存取* \[在中，選擇性\]
</dt> <dd>

使用者層級許可權的安全描述項。 安全描述項包含資源的許可權、擁有者和存取功能的相關資訊。 如需詳細資訊，請參閱 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)。

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

 

