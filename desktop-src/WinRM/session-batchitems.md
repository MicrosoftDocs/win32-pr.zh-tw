---
title: 'Session.BatchItems 屬性 (WSManDisp) '
description: 設定並取得每個列舉批次中的專案數。
ms.assetid: 1675ba12-a0c7-4e59-a013-2109780e8afe
ms.tgt_platform: multiple
keywords:
- BatchItems 屬性 Windows 遠端管理
- BatchItems 屬性 Windows 遠端管理，Session 物件
- Session 物件 Windows 遠端管理，BatchItems 屬性
topic_type:
- apiref
api_name:
- Session.BatchItems
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59e395eb27be2b922cf9d53e40f1d8cea0fc13a5dcf7b62b95ac606ec8f3f96f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795338"
---
# <a name="sessionbatchitems-property"></a>Session.BatchItems 屬性

設定並取得每個列舉批次中的專案數。 列舉期間無法變更此值。 資源提供者可能會設定限制。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
Session.BatchItems As long
```



## <a name="property-value"></a>屬性值

指定對服務的每個基礎網路呼叫傳回的專案數目上限。 預設值為 20。

## <a name="remarks"></a>備註

這是一項優化功能，可控制在用戶端與伺服器之間進行網路呼叫的頻率。 目前，它僅用於列舉。 如需列舉資源的詳細資訊，請參閱 [**列舉**](session-enumerate.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>WSManDisp。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>WSManDisp .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**會話**](session.md)
</dt> <dt>

[**列舉**](session-enumerate.md)
</dt> <dt>

[**列舉值. ReadItem**](enumerator-readitem.md)
</dt> </dl>

 

 





