---
description: 提供所有連接至電腦之平板電腦的存取權。
ms.assetid: d0fd9a6f-93fe-43d6-97fd-fee45854dfa1
title: ITabletManager 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletManager
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 3400d98a832819d1edd640cd78586f1cfb06bdee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027502"
---
# <a name="itabletmanager-interface"></a>ITabletManager 介面

提供所有連接至電腦之平板電腦的存取權。

## <a name="members"></a>成員

**ITabletManager** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **ITabletManager** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ITabletManager** 介面具有這些方法。



| 方法                                                  | 描述                                                        |
|:--------------------------------------------------------|:-------------------------------------------------------------------|
| [**GetTablet**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85))           | 抓取指定的 tablet 物件。<br/>                  |
| [**GetTabletCount**](itabletmanager-gettabletcount.md) | 抓取連接至系統的平板電腦數目。<br/> |



 

## <a name="remarks"></a>備註

開發人員不應使用此介面。

下列程式碼顯示如何實 **ITabletManager** 介面。

``` syntax
[
    object,
    uuid(764DE8AA-1867-47C1-8F6A-122445ABD89A),
    pointer_default(unique)
]
interface ITabletManager : IUnknown
{
    HRESULT GetDefaultTablet(
        [out] ITablet **ppTablet);

    HRESULT GetTabletCount(
        [out] ULONG *pcTablets);

    HRESULT GetTablet(
        [in] ULONG iTablet,
        [out] ITablet **ppTablet);

    HRESULT GetTabletContextById(
        [in] TABLET_CONTEXT_ID tcid,
        [out] ITabletContext **ppContext);

    HRESULT GetCursorById(
        [in] CURSOR_ID cid,
        [out] ITabletCursor **ppCursor);
};
        
        
```

呼叫 [](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)具有 CLSID TABLETMANAGERS 類別識別碼的 CoCreateInstance \_ ，然後呼叫 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))以取得 **ITabletManager 介面** 的指標。 CLSID \_ TABLETMANAGERS GUID 的定義如下：

``` syntax
#define CLSID_TabletManagerS uuid(A5B020FD-E04B-4e67-B65A-E7DEED25B2CF)
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                              |
| 程式庫<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

