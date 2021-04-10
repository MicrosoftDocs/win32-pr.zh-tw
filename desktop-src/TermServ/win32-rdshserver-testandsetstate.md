---
title: Win32_RDSHServer 類別的 TestAndSetState 方法
description: 比較目前的狀態與指定的比較元;如果兩者相符，則狀態會設定為新的值。 不論相符的結果為何，也會傳回目前的狀態。
ms.assetid: f1bb0076-251b-4c0d-92f9-1c460e1b26bb
ms.tgt_platform: multiple
keywords:
- TestAndSetState 方法遠端桌面服務
- TestAndSetState 方法遠端桌面服務，Win32_RDSHServer 類別
- Win32_RDSHServer 類別遠端桌面服務，TestAndSetState 方法
topic_type:
- apiref
api_name:
- Win32_RDSHServer.TestAndSetState
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ff4c9b616c2a288f5f39b240d71b2611e25d45f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103985"
---
# <a name="testandsetstate-method-of-the-win32_rdshserver-class"></a>Win32 RDSHServer 類別的 TestAndSetState 方法 \_

比較目前的狀態與指定的比較元;如果兩者相符，則狀態會設定為新的值。 不論相符的結果為何，也會傳回目前的狀態。

## <a name="syntax"></a>語法


```mof
uint32 TestAndSetState(
  [in]  uint32 Comparand,
  [in]  uint32 NewState,
  [out] uint32 InitState
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*比較元* \[在\]
</dt> <dd>

要與目前狀態比較的值;如果這兩個值相符，則狀態會設定為 *NewState*。

</dd> <dt>

*NewState* \[在\]
</dt> <dd>

狀態的新值。

</dd> <dt>

*InitState* \[擴展\]
</dt> <dd>

在成功或失敗時，會傳回目前的狀態。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                   |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                              |
| 命名空間<br/>                | 根 \\ cimv2 \\ rdm<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ RDSHServer**](win32-rdshserver.md)
</dt> </dl>

 

 





