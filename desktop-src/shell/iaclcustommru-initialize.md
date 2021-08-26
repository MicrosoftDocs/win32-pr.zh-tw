---
description: 從登錄將字串清單載入最近使用的 (MRU) 清單中。
title: IACLCustomMRU：： Initialize 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IACLCustomMRU.Initialize
api_type:
- COM
api_location: ''
ms.assetid: 358921b0-46c4-4428-b0b5-57a44fc3247b
ms.openlocfilehash: 0e0cad5f144a4ce97c648463cfdf31bf1c2ee7da0fb89b5508ce9386dba0f14f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111758"
---
# <a name="iaclcustommruinitialize-method"></a>IACLCustomMRU：： Initialize 方法

從登錄將字串清單載入最近使用的 (MRU) 清單中。

## <a name="syntax"></a>語法


```C++
HRESULT Initialize(
  [in] LPCWSTR pwszMRURegKey,
  [in] DWORD   dwMax
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pwszMRURegKey* \[在\]
</dt> <dd>

類型： **LPCWSTR**

緩衝區的指標，其中包含保存 MRU 清單字串的登錄機碼。

</dd> <dt>

*dwMax* \[在\]
</dt> <dd>

類型： **DWORD**

可從 *pwszMRURegKey* 取得的最大專案數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/> |



 

 




