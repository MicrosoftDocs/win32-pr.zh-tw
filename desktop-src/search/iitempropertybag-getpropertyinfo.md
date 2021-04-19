---
description: 取得讀取或儲存屬性包中的屬性所需的資訊。 只有在 Windows XP 和 Windows Server 2003 上才支援 IItemPropertyBag 介面，且不應再使用。
ms.assetid: 1667b67d-9dd2-48a6-81dd-c8b06834cef0
title: IItemPropertyBag：： GetPropertyInfo 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag.GetPropertyInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: a64b064c6c6d3708edc353db136fcad599d14adb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991810"
---
# <a name="iitempropertybaggetpropertyinfo-method"></a>IItemPropertyBag：： GetPropertyInfo 方法

取得讀取或儲存屬性包中的屬性所需的資訊。 只有在 Windows XP 和 Windows Server 2003 上才支援 [**IItemPropertyBag**](iitempropertybag.md) 介面，且不應再使用。

## <a name="syntax"></a>語法


```C++
HRESULT GetPropertyInfo(
  [in]  ULONG    iProperty,
  [in]  ULONG    cProperties,
  [out] ITEMPROP *pPropBag,
  [out] ULONG    *pcProperties
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*iProperty* \[在\]
</dt> <dd>

第一個屬性之以零為起始的索引，其為其所要求的資訊。

</dd> <dt>

*cProperties* \[在\]
</dt> <dd>

要取得資訊的屬性數目。 這個引數會指定 *pPropBag* 中的陣列元素數目。

</dd> <dt>

*pPropBag* \[擴展\]
</dt> <dd>

接收屬性資訊之 [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) 結構陣列的指標。

</dd> <dt>

*pcProperties* \[擴展\]
</dt> <dd>

接收 **ULONG** 變數的指標，此變數會接收已抓取資訊的屬性數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，它會傳回 S \_ OK。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

只有在 Windows XP 和 Windows Server 2003 上才支援 [**IItemPropertyBag**](iitempropertybag.md) 介面，且不應再使用。

若要在執行 Windows XP 或 Windows Server 2003 的電腦上使用協力廠商通訊協定處理常式來預覽附件，可能需要使用 [**IItemPropertyBag**](iitempropertybag.md) 介面和下列 Api： [**ISearchProtocolUI**](-search-isearchprotocolui.md)、 [**IItemPreviewerExt**](-search-iitempreviewerext.md) 和 [**ISearchItem**](-search-isearchitem.md) 介面、 [**LINKINFO**](-search-linkinfo.md) 和 [**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop) 結構，以及 [**LINKTYPE**](-search-linktype.md) 列舉。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP （含 SP2） \[ 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/> |
| 可轉散發套件<br/>          | Windows 桌面搜尋 (WDS) 3。0<br/>          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IItemPropertyBag**](iitempropertybag.md)
</dt> </dl>

 

 




