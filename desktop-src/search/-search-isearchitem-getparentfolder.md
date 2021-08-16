---
description: 如果 URL 代表實際的 Shell 資料來源 (也稱為 Shell 命名空間延伸) ，則取得 ISearchItem 物件。
ms.assetid: 7da6344d-b433-48c3-8f75-7bef0295b9ea
title: ISearchItem：： GetParentFolder 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchItem.GetParentFolder
api_type:
- COM
api_location: ''
ms.openlocfilehash: a5e5aded87ca197af8774a7b5506e21c958dc564eb0af67396e100877ac53e10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094908"
---
# <a name="isearchitemgetparentfolder-method"></a>ISearchItem：： GetParentFolder 方法

如果 URL 代表實際的 Shell 資料來源 (也稱為 Shell 命名空間延伸) ，則取得 [**ISearchItem**](-search-isearchitem.md) 物件。

## <a name="syntax"></a>語法


```C++
HRESULT GetParentFolder(
  [out] ppShellFolder **IShellFolder,
  [out] ppidl         *LPITEMIDLIST
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*IShellFolder* \[擴展\]
</dt> <dd>

類型： **ppShellFolder \* \***

傳回時，包含包含目前 URL 之資料夾的指標位址。 [IShellFolder 介面](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) 會由所有 Shell 命名空間資料夾物件公開，並使用其方法來管理資料夾。

</dd> <dt>

*LPITEMIDLIST* \[擴展\]
</dt> <dd>

類型： **ppidl \***

傳回時，包含識別父資料夾 (PIDL) 之專案識別碼清單的指標位址。 *LPITEMIDLIST* 參數可以參考命名空間階層中父資料夾底下任何層級的物件，因此可以是相對於上層資料夾之 **pidl** 的多層指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

只有 Windows XP 和 Windows Server 2003 才支援 **ISearchItem：： GetParentFolder** 方法，且不應再使用。

若要在執行 Windows XP 或 Windows Server 2003 的電腦上使用協力廠商通訊協定處理常式來預覽附件，可能需要使用 [**ISearchItem**](-search-isearchitem.md)介面和下列 api： [**IItemPreviewerExt**](-search-iitempreviewerext.md)、 [**IItemPropertyBag**](iitempropertybag.md)和 [**ISearchProtocolUI**](-search-isearchprotocolui.md)介面、 [**LINKINFO**](-search-linkinfo.md)結構和 [**LINKTYPE**](-search-linktype.md)列舉。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows只有 XP （含 SP2） \[ 桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/> |
| 可轉散發套件<br/>          | Windows (WDS 的桌面搜尋) 3。0<br/>          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ISearchItem**](-search-isearchitem.md)
</dt> </dl>

 

 
