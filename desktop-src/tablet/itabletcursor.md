---
description: 表示手寫筆物件。
ms.assetid: c55945b7-59df-49b5-b25f-fa96056889fc
title: ITabletCursor 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: eecbebc7090fb57d3794f3d056c24fba61fa5c61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852567"
---
# <a name="itabletcursor-interface"></a>ITabletCursor 介面

表示手寫筆物件。

## <a name="members"></a>成員

**ITabletCursor** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **ITabletCursor** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ITabletCursor** 介面具有這些方法。



| 方法                                                 | 描述                                                            |
|:-------------------------------------------------------|:-----------------------------------------------------------------------|
| [**GetButton**](itabletcursor-getbutton.md)           | 從 tablet 手寫筆取出指定的按鈕物件。<br/> |
| [**GetButtonCount**](itabletcursor-getbuttoncount.md) | 抓取 tablet 手寫筆上的按鈕數目。<br/>       |
| [**GetId**](itabletcursor-getid.md)                   | 抓取手寫筆識別碼。<br/>                            |
| [**GetName**](itabletcursor-getname.md)               | 捕獲 tablet 手寫筆的名稱。<br/>                    |
| [**IsInverted**](itabletcursor-isinverted.md)         | 指出手寫筆是否已反轉。<br/>                     |



 

## <a name="remarks"></a>備註

請勿使用這個介面。

下列程式碼說明如何定義 **ITabletCursor** 介面。

``` syntax
[
    object,
    uuid(EF9953C6-B472-4B02-9D22-D0E247ADE0E8,
    pointer_default(unique)
]
interface ITabletCursor : IUnknown
{
    HRESULT GetName(
        [out] LPWSTR *ppwszName);

    HRESULT IsInverted();

    HRESULT GetId(
        [out] CURSOR_ID *pCid);

    HRESULT GetTablet(
        [out] ITablet **ppTablet);

    HRESULT GetButtonCount(
        [out] ULONG *pcButtons);

    HRESULT GetButton(
        [in] ULONG iButton,
        [out] ITabletCursorButton **ppButton);
};

     
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                              |
| 程式庫<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

