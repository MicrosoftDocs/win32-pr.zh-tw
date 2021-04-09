---
description: 傳回具有使用者或群組所持有之共用的存取權限的 uint32 點陣圖，而該共用會傳回該實例。
ms.assetid: 1f656c63-f5ee-4b14-845a-0eb34a0e7a64
ms.tgt_platform: multiple
title: Win32_ClusterShare 類別的 GetAccessMask 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClusterShare.GetAccessMask
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: db27998c362e3df350dd12b6b91f3966cfc152ae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110509"
---
# <a name="getaccessmask-method-of-the-win32_clustershare-class"></a>Win32 ClusterShare 類別的 GetAccessMask 方法 \_

傳回具有使用者或群組所持有之共用的存取權限的 **uint32** 點陣圖，而該共用會傳回該實例。

## <a name="syntax"></a>語法


```mof
uint32 GetAccessMask();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

使用者或群組所持有之共用的存取權限。

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

 

 




