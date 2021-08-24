---
description: 填滿 IWiaItem2 介面的指標陣列。
ms.assetid: 35fd5bdf-7e6c-431f-a9c6-62a86ee05f95
title: 'IEnumWiaItem2：： Next 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.Next
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: cf884375f504bb801bcebcaad3f75b23c5f82956ce3a1d45dd5a50bfa5f8e53c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451138"
---
# <a name="ienumwiaitem2next-method"></a>IEnumWiaItem2：： Next 方法

填滿 [**IWiaItem2**](-wia-iwiaitem2.md) 介面的指標陣列。

## <a name="syntax"></a>語法


```C++
HRESULT Next(
  [in]      ULONG     cElt,
  [out]     IWiaItem2 **ppIWiaItem2,
  [in, out] ULONG     *pcEltFetched
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*cElt* \[在\]
</dt> <dd>

類型： **ULONG**

指定 *ppIWiaItem2* 參數所指定之陣列中的陣列元素數目。

</dd> <dt>

*ppIWiaItem2* \[擴展\]
</dt> <dd>

類型： **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

接收 [**IWiaItem2**](-wia-iwiaitem2.md) 介面指標陣列的位址。 **IEnumWiaItem2：： Next** 會使用介面指標填滿此陣列。

</dd> <dt>

*pcEltFetched* \[in、out\]
</dt> <dd>

類型： **ULONG \***

在輸出中，此參數會接收實際儲存在 *ppIWiaItem2* 參數所指出的陣列中的介面指標數目。 列舉完成時，此參數會包含零。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

Windows 的影像取得 (wia) 2.0 執行時間系統會將 wia 2.0 硬體裝置表示為 [**IWiaItem2**](-wia-iwiaitem2.md)物件的階層式樹狀結構。 應用程式會使用 **IEnumWiaItem2：： Next** 方法，為硬體裝置的 **IWiaItem2** 物件樹狀結構的目前資料夾中的每個專案取得 **IWiaItem2** 介面指標。

為了取得指標清單，應用程式會傳遞所配置之 [**IWiaItem2**](-wia-iwiaitem2.md) 介面指標的陣列。 它也會在參數 *cElt* 中傳遞陣列元素的數目。 **IEnumWiaItem2：： Next** 方法會使用 **IWiaItem2** 介面的指標來填滿陣列。

在列舉程式完成之前， **IEnumWiaItem2：： Next** 方法會傳回 S \_ OK。 它會在每次執行時，將 *pcEltFetched* 的值設定為它插入陣列中的專案數目。 當 **IEnumWiaItem2：： Next** 完成列舉 [**IWiaItem2**](-wia-iwiaitem2.md) 物件的程式時，它會傳回 \_ FALSE，並將 *pcEltFetched* 所指向的記憶體位置設定為零。

應用程式必須在透過 *ppIWiaItem2* 參數接收的介面指標上呼叫 [IUnknown：： Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia .idl</dt> </dl> |



 

 
