---
title: 'ResourceLocator. AddOption 方法 (WSManDisp .h) '
description: 新增處理要求所需的其他資料。 例如，某些 WMI 提供者可能需要具有提供者特定資訊的 IWbemCoNtext 或 SWbemNamedValueSet 物件。
ms.assetid: c85949fc-41e7-47eb-8aab-9b456490bc81
ms.tgt_platform: multiple
keywords:
- AddOption 方法 Windows 遠端管理
- AddOption 方法 Windows 遠端管理，ResourceLocator 物件
- ResourceLocator 物件 Windows 遠端管理，AddOption 方法
topic_type:
- apiref
api_name:
- ResourceLocator.AddOption
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 882f400dd2c59d2395dd2755846245f4e4ad385e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024745"
---
# <a name="resourcelocatoraddoption-method"></a>ResourceLocator. AddOption 方法

新增處理要求所需的其他資料。 例如，某些 WMI 提供者可能需要具有提供者特定資訊的 [**IWbemCoNtext**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) 或 [**SWbemNamedValueSet**](/windows/desktop/WmiSdk/swbemnamedvalueset) 物件。 您可以提供 [**ResourceLocator**](resourcelocator.md) 物件，而不是在 [**會話**](session.md) 物件作業中指定資源 URI，例如 [**session. Get**](session-get.md)、 [**session. Put**](session-put.md)或 [**Session。列舉**](session-enumerate.md)。

## <a name="syntax"></a>語法


```VB
ResourceLocator.AddOption( _
  ByVal OptionName, _
  ByVal OptionValue, _
  ByVal mustComply _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*選項名稱* \[在\]
</dt> <dd>

選擇性資料物件 (索引鍵) 的名稱。

</dd> <dt>

*OptionValue* \[在\]
</dt> <dd>

為選擇性資料物件提供的值。

</dd> <dt>

*mustComply* \[在\]
</dt> <dd>

指出必須處理選項的旗標。 預設值為 **False** (0) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

**IWSManResourceLocator：： AddOption** 是對應的 c + + 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>WSManDisp。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>WSManDisp .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

