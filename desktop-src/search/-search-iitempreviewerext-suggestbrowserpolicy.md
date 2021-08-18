---
description: 建議要套用至瀏覽器的安全性原則。
ms.assetid: 73541611-2024-4c33-ab03-e3204244c46c
title: IItemPreviewerExt：： SuggestBrowserPolicy 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.SuggestBrowserPolicy
api_type:
- COM
api_location: ''
ms.openlocfilehash: 84446b49ab723f161de8f148e95916202efe06176191e820ab8bafc88ed9158a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969757"
---
# <a name="iitempreviewerextsuggestbrowserpolicy-method"></a>IItemPreviewerExt：： SuggestBrowserPolicy 方法

建議要套用至瀏覽器的安全性原則。

## <a name="syntax"></a>語法


```C++
HRESULT SuggestBrowserPolicy(
  [in]          DWORD dwContext,
  [out, retval] DWORD *pdwFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwCoNtext* \[在\]
</dt> <dd>

類型： **DWORD**

作業的內容識別碼。 覆寫 *dwCoNtext* 預設值，將內容識別碼設定為您選擇的值。

</dd> <dt>

*pdwFlags* \[退出，retval\]
</dt> <dd>

類型： **DWORD \***

包含驗證檢查旗標之 DWORD 值的指標。 **BROWSERPOLICY 未 \_ 受信任的 \_ 內容** 旗標可停用任何可能的預覽，以執行腳本或 ActiveX。 參數 *pdwFlags* 不得為 **Null** 指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

只有 Windows XP 和 Windows Server 2003 才支援 [**IItemPreviewerExt**](-search-iitempreviewerext.md)介面，因此不應再使用。

若要在執行 Windows XP 或 Windows Server 2003 的電腦上使用協力廠商通訊協定處理常式來預覽附件，可能需要使用 [**IItemPreviewerExt**](-search-iitempreviewerext.md)介面和下列 api： [**ISearchProtocolUI**](-search-isearchprotocolui.md)、 [**IItemPropertyBag**](iitempropertybag.md)和 [**ISearchItem**](-search-isearchitem.md)介面、 [**LINKINFO**](-search-linkinfo.md)結構和 [**LINKTYPE**](-search-linktype.md)列舉。

強烈建議您不要使用 **BROWSERPOLICY \_ 不受信任的 \_ 內容** 旗標，以停用任何可能的預覽功能來執行腳本或 ActiveX。 **IItemPreviewerExt：： SuggestBrowserPolicy** 方法可以傳回所預覽專案是否受信任的資訊。 這可讓預覽 trident 控制項執行腳本，甚至 ActiveX 控制項。 因為預覽程式通常會使用暫存檔案來產生預覽，所以這樣做可能會導致在本機電腦區域中出現未預期的腳本和程式碼執行。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows只有 XP （含 SP2） \[ 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/> |
| 可轉散發套件<br/>          | Windows (WDS 的桌面搜尋) 3。0<br/>          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IItemPreviewerExt**](-search-iitempreviewerext.md)
</dt> </dl>

 

 




