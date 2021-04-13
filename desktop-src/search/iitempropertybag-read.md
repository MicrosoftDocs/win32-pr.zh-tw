---
description: 使一或多個屬性從屬性包中讀取。 只有在 Windows XP 和 Windows Server 2003 上才支援 IItemPropertyBag 介面，且不應再使用。
ms.assetid: 78a63ef0-1b79-4b07-9121-a6fbd1116c4b
title: IItemPropertyBag：： Read 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPropertyBag.Read
api_type:
- COM
api_location: ''
ms.openlocfilehash: ef7af13dc42239a2823d7e7ca9b8def4748519fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318152"
---
# <a name="iitempropertybagread-method"></a>IItemPropertyBag：： Read 方法

使一或多個屬性從屬性包中讀取。 只有在 Windows XP 和 Windows Server 2003 上才支援 [**IItemPropertyBag**](iitempropertybag.md) 介面，且不應再使用。

## <a name="syntax"></a>語法


```C++
HRESULT Read(
  [in]  ULONG    cProperties,
  [in]  ITEMPROP *pPropBag,
  [out] VARIANT  *pvarValue,
  [out] HRESULT  *phrError
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*cProperties* \[在\]
</dt> <dd>

要讀取的屬性數目。 這個引數會指定陣列中 *pPropBag*、 *pvarValue* 和 *phrError* 的元素數目。

</dd> <dt>

*pPropBag* \[在\]
</dt> <dd>

[**ITEMPROP**](/windows/desktop/api/subsmgr/ns-subsmgr-itemprop)結構陣列的指標，指定所要求的屬性。

</dd> <dt>

*pvarValue* \[擴展\]
</dt> <dd>

接收傳回 **VARIANT** 結構陣列的指標，此陣列會接收屬性值。

</dd> <dt>

*phrError* \[擴展\]
</dt> <dd>

**HRESULT** 值陣列的指標，這些值會接收每個讀取之屬性的結果。 此陣列中至少必須有 *cProperties* 元素。

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

 

 




