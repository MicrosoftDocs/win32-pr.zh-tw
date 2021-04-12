---
description: 叫用驅動程式分割篩選，並將 IWiaPreview：： GetNewPreview 方法快取的未篩選影像傳遞至篩選。
ms.assetid: 4ae817b5-7091-432e-b004-0e53ae14fdb2
title: 'IWiaPreview：:D etectRegions 方法 (Wia. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.DetectRegions
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 40665d2aae6e1e2dffa4356540afb05d45050492
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191400"
---
# <a name="iwiapreviewdetectregions-method"></a>IWiaPreview：:D etectRegions 方法

叫用驅動程式分割篩選，並將 [**IWiaPreview：： GetNewPreview**](-wia-iwiapreview-getnewpreview.md) 方法快取的未篩選影像傳遞至篩選。

## <a name="syntax"></a>語法


```C++
HRESULT DetectRegions(
  [in] LONG lFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lFlags* \[在\]
</dt> <dd>

類型： **LONG**

未使用。 設定為零 (0) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

這個方法可以傳回其中一個值。



| 傳回碼                                                                               | Description                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>      | 作業成功。<br/>              |
| <dl> <dt>**E \_ >NOTIMPL**</dt> </dl> | 驅動程式不支援分割。<br/> |
| <dl> <dt>**否則**</dt> </dl>  | 標準 COM 錯誤碼。<br/>                |



 

## <a name="remarks"></a>備註

應用程式必須先呼叫 [**IWiaPreview：： GetNewPreview**](-wia-iwiapreview-getnewpreview.md) ，才能呼叫此函式。

當 Windows 映像取得 (WIA) 2.0 Preview 元件呼叫 **IWiaPreview：:D etectregions** 時，它會叫用驅動程式分割篩選，並傳遞先前傳遞給 [**IWiaPreview：： GetNewPreview**](-wia-iwiapreview-getnewpreview.md)的 [**IWiaItem2**](-wia-iwiaitem2.md)介面。 它也會將內部快取的影像傳遞至篩選。 分割篩選器會使用快取的影像來建立子範圍。

如果應用程式在呼叫 [**IWiaPreview：： GetNewPreview**](-wia-iwiapreview-getnewpreview.md)之後變更 [**IWiaItem2**](-wia-iwiaitem2.md)介面的任何屬性，則必須先還原原始屬性，應用程式才能呼叫 **IWiaPreview：:D etectregions**。 使用 [**GetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) 和 [**SetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream) 還原原始屬性。

**IWiaPreview：:D etectregions** 用來判斷快取影像的「子領域」。 針對每個偵測到的子領域，會在 [**IWiaItem2**](-wia-iwiaitem2.md) 介面下建立新的子 WIA 2.0 專案。 針對每個子專案，分割篩選必須設定下列 WIA 2.0 屬性的值： WIA \_ ip \_ XPOS、wia \_ IP \_ YPOS、WIA \_ ips \_ 範圍和 wia \_ ips \_ YEXTENT。 \_ \_ \_ \_ \_ \_ 如果驅動程式支援消除扭曲，則更高階的篩選會設定其他 wia 2.0 屬性，例如 WIA ip 反扭曲 X 和 wia ip。 WIA \_ ip \_ XPOS、wia \_ IP \_ YPOS、WIA \_ ips \_ 範圍和 wia \_ ips \_ YEXTENT 屬性代表要掃描之區域的周框。

驅動程式可能不支援分割。 在呼叫 **IWiaPreview：:D etectregions** 之前，應用程式通常會檢查驅動程式是否支援 WIA \_ ip \_ 分割屬性。 如果未執行屬性，則不支援分割，而且 **IWiaPreview：:D etectregions** 失敗，並傳回 E \_ >notimpl。

應用程式必須清除透過呼叫 **IWiaPreview：:D etectregions** 所建立的子專案。 例如，如果應用程式在相同的專案上對 **IWiaPreview：:D etectregions** 進行額外的呼叫，就必須清除先前的子專案。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia .idl</dt> </dl> |



 

 




