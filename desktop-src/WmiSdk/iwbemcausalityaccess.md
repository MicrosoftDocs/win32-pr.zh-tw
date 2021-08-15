---
description: 持續追蹤從父要求產生的子要求。
ms.assetid: e1d98eae-6fc1-489b-aa8b-2e86bac5c65a
ms.tgt_platform: multiple
title: 'IWbemCausalityAccess 介面 (Wbemint .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemCausalityAccess
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: a8c71d5b5f59a3b59fe3b639104bfa1fa2dcf9cd35764e37984759827ff7e92b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131390"
---
# <a name="iwbemcausalityaccess-interface"></a>IWbemCausalityAccess 介面

**IWbemCausalityAccess** 介面會持續追蹤從父要求產生的子要求。 您可以針對 [**IWbemCoNtext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext)使用 (QI) 的查詢介面，來取得 **IWbemCausalityAccess** 物件。 每個要求都是由全域唯一識別碼 (GUID) 來識別，而且可以有父要求或可能是最上層要求。 GUID 是唯一的128位數位。 例如，5b2fc63a-8af4-44cb-960c-aefdced908d6。

## <a name="members"></a>成員

**IWbemCausalityAccess** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IWbemCausalityAccess** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IWbemCausalityAccess** 介面具有這些方法。



| 方法                                                    | 描述                                                                                                                                                             |
|:----------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetRequestId**](iwbemcausalityaccess-getrequestid.md) | 傳回要求的唯一 GUID 識別碼。<br/>                                                                                                              |
| [**IsChildOf**](iwbemcausalityaccess-ischildof.md)       | 判斷要求是否為指定之父系要求的子系。 父要求可以有多個子要求，每個要求都是由唯一的 GUID 值所識別。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Wbemint。h</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>Fastprox.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[適用于 WMI 的 COM API](com-api-for-wmi.md)
</dt> </dl>

 

