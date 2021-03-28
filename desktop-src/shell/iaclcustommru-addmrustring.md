---
description: 將專案新增至最近使用的 (MRU) 清單中。
title: IACLCustomMRU：： AddMRUString 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IACLCustomMRU.AddMRUString
api_type:
- COM
api_location: ''
ms.assetid: d8fb8fa5-452b-45fd-b015-d9bf3d0c642e
ms.openlocfilehash: d2f444041f466b367f3d4532f65029bcc69c3683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991542"
---
# <a name="iaclcustommruaddmrustring-method"></a>IACLCustomMRU：： AddMRUString 方法

將專案新增至最近使用的 (MRU) 清單中。

## <a name="syntax"></a>語法


```C++
HRESULT AddMRUString(
  [in] LPCWSTR pwszEntry
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pwszEntry* \[在\]
</dt> <dd>

類型： **LPCWSTR**

包含新專案之緩衝區的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/> |



 

 




