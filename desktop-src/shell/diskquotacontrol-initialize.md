---
description: 開啟指定的磁片區，並初始化其配額控制物件。
ms.assetid: 20eae2a3-f602-48a2-bf1c-65570e7a5d21
title: DiskQuotaControl.Initialize 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.Initialize
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 0df879c626ccdac7494077f021c23a6e42b24f0df3aa780d1be8b1af8225527a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119455898"
---
# <a name="diskquotacontrolinitialize-method"></a>DiskQuotaControl.Initialize 方法

開啟指定的磁片區，並初始化其配額控制物件。

## <a name="syntax"></a>語法


```JScript
DiskQuotaControl.Initialize(
  sPath,
  bReadWrite
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*sPath* 
</dt> <dd>

類型： **字串**

字串值，包含要初始化之磁片區的完整路徑。

</dd> <dt>

*bReadWrite* 
</dt> <dd>

類型： **布林值**

指定如何開啟磁片區的布林值。 將 *bReadWrite* 設為 **TRUE** 以進行讀取/寫入存取，或設定為 **FALSE** 表示唯讀存取。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (5.0 版或更新版本) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DiskQuotaControl 物件**](diskquotacontrol-object.md)
</dt> </dl>

 

 




