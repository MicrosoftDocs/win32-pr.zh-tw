---
description: '\_當地址的狀態變更在應用程式目前開啟的行上時，就會傳送 TAPI 線路 ADDRESSSTATE 訊息。 應用程式可以叫用 lineGetAddressStatus 來判斷位址的目前狀態。'
ms.assetid: af211fa1-79f8-49ac-a1d8-b62981f50519
title: 'LINE_ADDRESSSTATE 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d85b42f6957487ff24706485bd09d1d47880fe9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994026"
---
# <a name="line_addressstate-message"></a>行 \_ ADDRESSSTATE 訊息

當地址的狀態變更在應用程式目前開啟的行上時，就會傳送 TAPI **線路 \_ ADDRESSSTATE** 訊息。 應用程式可以叫用 [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus) 來判斷位址的目前狀態。


```C++
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*hDevice* 
</dt> <dd>

線路裝置的控制碼。

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

開啟行時所提供的回呼實例。

</dd> <dt>

*dwParam1* 
</dt> <dd>

已變更狀態之位址的位址識別碼。

</dd> <dt>

*dwParam2* 
</dt> <dd>

變更的位址狀態。 可以是一或多個 [**LINEADDRESSSTATE \_ 常數**](lineaddressstate--constants.md)。

</dd> <dt>

*dwParam3* 
</dt> <dd>

未使用的。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

**該行 \_ ADDRESSSTATE** 訊息會傳送至已開啟行裝置且已啟用此訊息的任何應用程式。 您可以使用 [**lineGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages) 和 [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages)來控制和查詢不同狀態專案的這項訊息傳送。 預設會停用 [位址狀態報表]。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tapi</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)
</dt> <dt>

[**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)
</dt> <dt>

[**lineGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages)
</dt> <dt>

[**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages)
</dt> </dl>

 

 




