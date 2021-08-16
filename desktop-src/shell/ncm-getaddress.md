---
description: 指出網路位址是否符合指定的類型和格式。
title: 'NCM_GETADDRESS 訊息 (Shellapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 733CD62D-614C-4ac2-986D-CCFCFF4B1B4D
api_name:
- NCM_GETADDRESS
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 27f5beec56a0125d26cc359f40b5033eda1f035f2dec7666725264ec6fd59ba7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117677966"
---
# <a name="ncm_getaddress-message"></a>NCM \_ GETADDRESS 訊息

指出網路位址是否符合指定的類型和格式。


```C++
NCM_GETADDRESS

    wParam = (WPARAM) (PNC_ADDRESS) pv;

    lParam = 0;            

            
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*pv* \[in、out\]
</dt> <dd>如果已驗證 *hwnd* 所指定之控制項中的位址格式和類型，則為用來接收剖析格式之網路位址資訊的 <a href="/windows/win32/api/shellapi/ns-shellapi-nc_address">NC_ADDRESS</a>結構指標。 呼叫應用程式負責配置此結構的記憶體。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列其中一個 **HRESULT** 型別的值。



| 傳回碼                                                                                                | 描述                                                                                          |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>               | 呼叫應用程式無法配置 [**NC \_ 位址**](/windows/win32/api/shellapi/ns-shellapi-nc_address) 結構。<br/> |
| <dl> <dt>**\_緩衝區不足的錯誤 \_**</dt> </dl> | 輸出緩衝區太小，無法容納已剖析的網路位址。<br/>                           |
| <dl> <dt>**錯誤 \_ 不正確 \_ 參數**</dt> </dl>   | 網路位址字串不是任何指定的類型。<br/>                                  |
| <dl> <dt>**錯誤 \_ 成功**</dt> </dl>              | 作業成功。<br/>                                                             |
| <dl> <dt>**S \_ FALSE**</dt> </dl>                    | 網路位址控制中沒有要驗證的位址。<br/>                           |



 

## <a name="remarks"></a>備註

使用 **NCM \_ GETADDRESS** 訊息，針對預設的網路位址類型遮罩，驗證網路位址控制項中的網路位址。 若要具現化，請使用 Shellapi 中所定義的類別 **msctls \_ netaddress** 。 請在執行時間呼叫 [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) ，然後再傳送此訊息。 這會初始化包含網路位址控制項的通用控制項程式庫。

此訊息會從網路位址控制項取得網路位址字串、剖析字串，並檢查字串是否符合網路位址類型遮罩。 如果字串符合遮罩，訊息會傳回 S OK，並以剖析的 \_ 形式將字串傳回給呼叫的應用程式 (包括埠號碼、前置長度和其他位址資訊) 使用 *pv* 所指向的 [**NC \_ 位址**](/windows/win32/api/shellapi/ns-shellapi-nc_address)結構。 \_如果呼叫的應用程式無法配置 *pv* 所指向的結構，則此訊息會傳回 E INVALIDARG。

網際網路通訊協定的標記法 (IP) 位址版本4和 6 (v4/v6) 適用于服務和網路，以及使用網域名稱系統 (DNS) 格式的命名網際網路位址和服務。 如果網路位址字串代表 (DNS) 或服務的名稱主機名稱，則 [**NC \_ 位址**](/windows/win32/api/shellapi/ns-shellapi-nc_address)之 **PrefixLength** 成員中傳回的值為零。

請先使用 [**NCM \_ SETALLOWTYPE**](ncm-setallowtype.md) 訊息設定網路位址類型遮罩，然後再傳送 **NCM \_ GETADDRESS** 宏。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Shellapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**NCM \_ GETALLOWTYPE**](ncm-getallowtype.md)
</dt> <dt>

[**NetAddr \_ GetAddress**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getaddress)
</dt> </dl>

 

 




