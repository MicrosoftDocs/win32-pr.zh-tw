---
description: 允許延伸至屬性的豐富內容。
ms.assetid: d1b09ea0-7263-4b7c-8c59-25251bb6b285
title: IItemPreviewerExt：： GetLinkedContent 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.GetLinkedContent
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7d450bbda2ac7c24b49d1ca5032fd1c59754652e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972821"
---
# <a name="iitempreviewerextgetlinkedcontent-method"></a>IItemPreviewerExt：： GetLinkedContent 方法

允許延伸至屬性的豐富內容。

## <a name="syntax"></a>語法


```C++
HRESULT GetLinkedContent(
  [in]          DWORD     dwContext,
  [in]          LPCOLESTR pwszProp,
  [out, retval] LINKINFO  *pInfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwCoNtext* \[在\]
</dt> <dd>

類型： **DWORD**

作業的內容識別碼。 覆寫 *dwCoNtext* 預設值，將內容識別碼設定為您選擇的值。

</dd> <dt>

*pwszProp* \[在\]
</dt> <dd>

類型： **LPCOLESTR**

作為 Unicode 字串之連結內容的屬性指標。

</dd> <dt>

*pInfo* \[退出，retval\]
</dt> <dd>

類型： **[**LINKINFO**](-search-linkinfo.md) \** _

接收 [_ *LINKINFO* *](-search-linkinfo.md)結構的指標，此結構的方法會傳回交易的相關資訊。 *pInfo* 不得為 **Null** 指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

只有在 Windows XP 和 Windows Server 2003 上才支援 [**IItemPreviewerExt**](-search-iitempreviewerext.md) 介面，且不應再使用。

若要在執行 Windows XP 或 Windows Server 2003 的電腦上使用協力廠商通訊協定處理常式來預覽附件，可能需要使用 [**IItemPreviewerExt**](-search-iitempreviewerext.md) 介面和下列 Api： [**ISearchProtocolUI**](-search-isearchprotocolui.md)、 [**IItemPropertyBag**](iitempropertybag.md) 和 [**ISearchItem**](-search-isearchitem.md) 介面、 [**LINKINFO**](-search-linkinfo.md) 結構和 [**LINKTYPE**](-search-linktype.md) 列舉。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP （含 SP2） \[ 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/> |
| 可轉散發套件<br/>          | Windows 桌面搜尋 (WDS) 3。0<br/>          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IItemPreviewerExt**](-search-iitempreviewerext.md)
</dt> </dl>

 

 




