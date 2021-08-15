---
description: 取得要內嵌至輸出 MHTML 資料流程的相關主體部分。
ms.assetid: 7810568b-5fb7-4814-aa9f-d7ae805c97e1
title: IItemPreviewerExt：： GetRelatedPart 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.GetRelatedPart
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9abc4415eef014697376c9df4b89af47037a99df5c9ab5a3c74a3d7825b344c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863971"
---
# <a name="iitempreviewerextgetrelatedpart-method"></a>IItemPreviewerExt：： GetRelatedPart 方法

取得要內嵌至輸出 MHTML 資料流程的相關主體部分。

## <a name="syntax"></a>語法


```C++
HRESULT GetRelatedPart(
  [in]          DWORD     dwContext,
  [in]          LPCOLESTR pwszProp,
  [in]          DWORD     dwIndex,
  [out, retval] LINKINFO  *pInfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwCoNtext* \[在\]
</dt> <dd>

類型： **DWORD**

作業的內容識別碼。 覆寫 **dwCoNtext** 預設值，將內容識別碼設定為您選擇的值。

</dd> <dt>

*pwszProp* \[在\]
</dt> <dd>

類型： **LPCOLESTR**

作為 Unicode 字串之連結內容的屬性指標。

</dd> <dt>

*dwIndex* \[在\]
</dt> <dd>

類型： **DWORD**

不帶正負號的長整數值，其中包含相關主體部分以零為起始的索引。

</dd> <dt>

*pInfo* \[退出，retval\]
</dt> <dd>

類型： **[ **LINKINFO**](-search-linkinfo.md)\***

接收 [**LINKINFO**](-search-linkinfo.md) 結構的指標，該結構的方法會傳回交易的相關資訊。 *pInfo* 不得為 **Null** 指標。

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

 

 




