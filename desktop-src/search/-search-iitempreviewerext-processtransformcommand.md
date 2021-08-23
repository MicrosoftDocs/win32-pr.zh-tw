---
description: 允許處理在預覽範本中遇到的轉換命令。
ms.assetid: 0b81b780-8bd1-4667-a0a1-65319f209603
title: IItemPreviewerExt：:P rocessTransformCommand 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.ProcessTransformCommand
api_type:
- COM
api_location: ''
ms.openlocfilehash: f93d4be0bf9491c4fd2f6074c00692d6f634704ec820a34baeb4f1d52343c36a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969771"
---
# <a name="iitempreviewerextprocesstransformcommand-method"></a>IItemPreviewerExt：:P rocessTransformCommand 方法

允許處理在預覽範本中遇到的轉換命令。

## <a name="syntax"></a>語法


```C++
HRESULT ProcessTransformCommand(
  [in]          DWORD     dwContext,
  [in]          LPCOLESTR pwszName,
  [in]          LPCOLESTR pwszArg,
  [out, retval] VARIANT   *pvarResult
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwCoNtext* \[在\]
</dt> <dd>

類型： **DWORD**

作業的內容識別碼。 覆寫 *dwCoNtext* 預設值，將內容識別碼設定為您選擇的值。

</dd> <dt>

*pwszName* \[在\]
</dt> <dd>

類型： **LPCOLESTR**

轉換命令名稱的指標，作為 Unicode 字串。

</dd> <dt>

*pwszArg* \[在\]
</dt> <dd>

類型： **LPCOLESTR**

引數的指標，作為 Unicode 字串。

</dd> <dt>

*pvarResult* \[退出，retval\]
</dt> <dd>

類型： **VARIANT \***

結果 variant 的指標。 *pvarResult* 不得為 **Null** 指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

只有 Windows XP 和 Windows Server 2003 才支援 [**IItemPreviewerExt**](-search-iitempreviewerext.md)介面，因此不應再使用。

若要在執行 Windows XP 或 Windows Server 2003 的電腦上使用協力廠商通訊協定處理常式來預覽附件，可能需要使用 [**IItemPreviewerExt**](-search-iitempreviewerext.md)介面和下列 api： [**ISearchProtocolUI**](-search-isearchprotocolui.md)、 [**IItemPropertyBag**](iitempropertybag.md)和 [**ISearchItem**](-search-isearchitem.md)介面、 [**LINKINFO**](-search-linkinfo.md)結構和 [**LINKTYPE**](-search-linktype.md)列舉。

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

 

 




