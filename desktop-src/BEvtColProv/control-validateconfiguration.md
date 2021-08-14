---
description: 驗證設定文字的正確性，而不將其設定為使用中。 在成功時傳回1，錯誤則為0。
ms.assetid: baeabed0-7717-498a-9886-e49e4a101711
ms.tgt_platform: multiple
title: Control 類別的 ValidateConfiguration 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.ValidateConfiguration
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: a6daf61721534cf61f76c97b76d5929fb047ef6ddc8f8ee000a107dace426a3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118173941"
---
# <a name="validateconfiguration-method-of-the-control-class"></a>Control 類別的 ValidateConfiguration 方法

驗證設定文字的正確性，而不將其設定為使用中。 在成功時傳回1，錯誤則為0。

## <a name="syntax"></a>語法


```mof
Uint32 ValidateConfiguration(
  [in]  string Config,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Config* \[在\]
</dt> <dd>

要檢查的設定。

</dd> <dt>

*ErrorString* \[擴展\]
</dt> <dd>

當此方法傳回時，如果發生錯誤，此參數會包含作業之驗證錯誤的描述。

</dd> <dt>

*WarningString* \[擴展\]
</dt> <dd>

當此方法傳回時，此參數會包含作業之任何驗證警告的描述。

具有警告的文字字串。

</dd> <dt>

*InfoString* \[擴展\]
</dt> <dd>

當此方法傳回時，此參數會包含一組有關設定的資訊。

</dd> <dt>

*ErrorType* \[擴展\]
</dt> <dd>

當此方法傳回時，如果發生驗證錯誤，此參數會指出錯誤類型。

可能的值包括：

<dt>

0
</dt> <dd>

遺漏引數。

</dd> <dt>

1
</dt> <dd>

引數格式無效。

</dd> <dt>

2
</dt> <dd>

設定引數無效。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

<dl> <dt>


</dt> <dd>

0

失敗

</dd> <dt>


</dt> <dd>

1

Success

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                                          |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                                       |
| 命名空間<br/>                | 根 \\ Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**控制**](control.md)
</dt> </dl>

 

 




