---
title: 'IADsNameTranslate 屬性方法 (Iads .h) '
description: 設定 ChaseReferral 屬性。
ms.assetid: 7c44fe9b-16a5-4bd5-a80b-8f3dcfec20cc
ms.tgt_platform: multiple
keywords:
- IADsNameTranslate 屬性方法 ADSI
topic_type:
- apiref
api_name:
- IADsNameTranslate Property Methods
- IADsNameTranslate.ChaseReferral
- IADsNameTranslate.put_ChaseReferral
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b90d068da3b8dca1bbcae361d1dbacafcf44464
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934815"
---
# <a name="iadsnametranslate-property-methods"></a>IADsNameTranslate 屬性方法

[**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate)介面的 property 方法會設定 **ChaseReferral** 屬性。 如需詳細資訊，請參閱 [介面屬性方法](interface-property-methods.md)。

## <a name="properties"></a>屬性

<dl> <dt>

**ChaseReferral**
</dt> <dd> <dl>

在 ADS 中定義的參考追蹤選項會追蹤 [**\_ \_ 參考 \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum)。 設定參考追蹤時，會在不屬於這個目錄的物件上執行名稱轉譯，而這些物件則是從參考追蹤傳回的參考。

<dt>

存取類型：僅限寫入
</dt> <dt>

編寫資料類型的腳本： **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT put_ChaseReferral(
  [in] LONG lnChaseReferral
);
```


</dt> </dl> </dd> </dl>

 

## <a name="remarks"></a>備註

只有當您使用 [**IADsNameTranslate：： Set**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-set) 和 [**IADsNameTranslate：： Get**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-get)時，才適用參考追蹤選項。 [**IADsNameTranslate：： SetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-setex)或 [**IADsNameTranslate：： GetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-getex)無法使用此功能。

[**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate)介面具有部分實作為廣告的部分執行，會透過 **ChaseReferral** 屬性來進行 [**\_ \_ 參考 \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum)。 如果 [ **ChaseReferral** ] 屬性設定為 [零] (0) ，則與指定廣告的 [ **\_ \_ \_ 永遠不** (0) ] 相同。 如果使用非零值，則與指定 **廣告 \_ \_ \_ 一律** (0x60) 相同。 **IADsNameTranslate** 不會執行 **廣告將 \_ \_ 參考 \_ 附屬** (0x20) 或 ADS 會 (0x40) 選項來進行 **\_ \_ 參考 \_** 。

已啟用參考追蹤的預設設定 (**ADS 會 \_ \_ \_ 一律**) 。 如果沒有參考追蹤，您可以在僅限連線目錄伺服器的物件上執行名稱轉譯。 如果您不確定感興趣的物件是否在指定的伺服器上，您應該將此屬性設定為 **ADS \_ \_ \_ 一律** 會進行參考。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Iads。h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsNameTranslate 定義為 B1B272A3-3625-11D1-A3A4-00C04FB950DC<br/>    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**廣告會將 \_ \_ 參考 \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum)
</dt> <dt>

[**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate)
</dt> <dt>

[**IADsNameTranslate：： Get**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-get)
</dt> <dt>

[**IADsNameTranslate::GetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-getex)
</dt> <dt>

[**IADsNameTranslate：： Set**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-set)
</dt> <dt>

[**IADsNameTranslate::SetEx**](/windows/desktop/api/Iads/nf-iads-iadsnametranslate-setex)
</dt> <dt>

[介面屬性方法](interface-property-methods.md)
</dt> </dl>

 

 





