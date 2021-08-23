---
description: 取得指定之資料的搜尋專案。 針對收集程式所處理的每個 URL，會呼叫這個方法一次，並抓取 ISearchItem 物件的指標。
ms.assetid: 35893bc9-8327-44f9-a9fc-7855c5c063e3
title: ISearchProtocolUI：： GetSearchItemForUrl 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchProtocolUI.GetSearchItemForUrl
api_type:
- COM
api_location: ''
ms.openlocfilehash: 8636f42026fe44131e149b0e378089b70c7d4f49b9e23b5d48ebe50aa5721d79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119594808"
---
# <a name="isearchprotocoluigetsearchitemforurl-method"></a>ISearchProtocolUI：： GetSearchItemForUrl 方法

取得指定之資料的搜尋專案。 針對收集程式所處理的每個 URL，會呼叫這個方法一次，並抓取 [**ISearchItem**](-search-isearchitem.md) 物件的指標。

## <a name="syntax"></a>語法


```C++
HRESULT GetSearchItemForUrl(
  [in]          LPCOLESTR        pcwszURL,
  [in]          IItemPropertyBag *pPropertyBag,
  [out, retval] ISearchItem      **ppSearchItem
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pcwszURL* \[在\]
</dt> <dd>

類型： **LPCOLESTR**

Null 資料終止的 Unicode 字串指標，其中包含要存取之 URL 的搜尋專案。

</dd> <dt>

*pPropertyBag* \[在\]
</dt> <dd>

類型： **IItemPropertyBag \***

[**IItemPropertyBag**](iitempropertybag.md)物件的指標，其中包含搜尋專案的相關資訊，包括專案的屬性。

</dd> <dt>

*ppSearchItem* \[退出，retval\]
</dt> <dd>

類型： **[ **ISearchItem**](-search-isearchitem.md)\*\***

接收這個方法所建立之 [**ISearchItem**](-search-isearchitem.md) 物件的指標位址。 此物件包含搜尋專案的相關資訊，例如專案的檔案名。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

只有 Windows XP 和 Windows Server 2003 才支援 **ISearchProtocolUI：： GetSearchItemForUrl** 方法，且不應再使用。

若要在執行 Windows XP 或 Windows Server 2003 的電腦上使用協力廠商通訊協定處理常式來預覽附件，可能需要使用 [**ISearchProtocolUI**](-search-isearchprotocolui.md)介面和下列 api： [**IItemPreviewerExt**](-search-iitempreviewerext.md)、 [**IItemPropertyBag**](iitempropertybag.md)和 [**ISearchItem**](-search-isearchitem.md)介面、 [**LINKINFO**](-search-linkinfo.md)結構和 [**LINKTYPE**](-search-linktype.md)列舉。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows只有 XP （含 SP2） \[ 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/> |
| 可轉散發套件<br/>          | Windows (WDS 的桌面搜尋) 3。0<br/>          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ISearchProtocolUI**](-search-isearchprotocolui.md)
</dt> </dl>

 

 




