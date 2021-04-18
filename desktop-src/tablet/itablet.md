---
description: 代表連接到電腦的平板電腦。
ms.assetid: 31e11f7d-5610-4c49-9203-2dc322fbef95
title: ITablet 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 76fa7baea2713e5a2e5eaae562b6dac29e002fff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971495"
---
# <a name="itablet-interface"></a>ITablet 介面

代表連接到電腦的平板電腦。

## <a name="members"></a>成員

**ITablet** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **ITablet** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ITablet** 介面具有這些方法。



| 方法                                                                 | 描述                                                                           |
|:-----------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**CreateCoNtext**](itablet-createcontext.md)                         | 建立描述指定之平板電腦裝置的內容物件。<br/>       |
| [**GetCursor**](/previous-versions/windows/desktop/legacy/aa373535(v=vs.85))                                 | 抓取指定的 [**ITabletCursor**](itabletcursor.md) 物件。<br/>     |
| [**GetCursorCount**](itablet-getcursorcount.md)                       | 捕獲與平板電腦相關聯的資料指標物件數目。<br/>         |
| [**GetDefaultCoNtextSettings**](itablet-getdefaultcontextsettings.md) | 捕獲平板電腦的預設內容設定。<br/>                     |
| [**GetHardwareCaps**](itablet-gethardwarecaps.md)                     | 抓取代表平板電腦硬體功能的值。<br/> |
| [**GetMaxInputRect**](itablet-getmaxinputrect.md)                     | 抓取代表平板電腦最大輸入區域的矩形。<br/>    |
| [**GetName**](itablet-getname.md)                                     | 抓取包含 tablet 裝置名稱的字串。<br/>               |
| [**GetPlugAndPlayId**](itablet-getplugandplayid.md)                   | 抓取包含平板電腦裝置之隨插即用識別碼的字串。<br/>  |
| [**GetPropertyMetrics**](/previous-versions/windows/desktop/legacy/aa367722(v=vs.85))               | 取得指定之屬性的度量資料。<br/>                       |



 

## <a name="remarks"></a>備註

開發人員不應使用此介面。

下列程式碼說明如何定義 **ITablet** 介面。

``` syntax
[
    object,
   uuid(1CB2EFC3-ABC7-4172-8FCB-3BC9CB93E29F),
    pointer_default(unique)
]
interface ITablet : IUnknown
{
    HRESULT GetDefaultContextSettings(
        [out] TABLET_CONTEXT_SETTINGS **ppTCS);

    HRESULT CreateContext(
        [in] HWND hWnd,
        [in, unique] RECT *prcInput,
        [in] DWORD dwOptions,
        [in, unique] TABLET_CONTEXT_SETTINGS *pTCS,
        [in] CONTEXT_ENABLE_TYPE cet,
        [out] ITabletContext **ppCtx,
        [in, out, unique] TABLET_CONTEXT_ID *pTcid,
        [in, out, unique] PACKET_DESCRIPTION **ppPD,
        [in, unique] ITabletEventSink *pSink);

    HRESULT GetName(
        [out] LPWSTR *ppwszName);

    HRESULT GetMaxInputRect(
        [out] RECT *prcInput);

    HRESULT GetHardwareCaps(
        [out] DWORD *pdwCaps);

    HRESULT GetPropertyMetrics(
        [in] REFGUID rguid,
        [out] PROPERTY_METRICS *pPM);

    HRESULT GetPlugAndPlayId(
        [out] LPWSTR *ppwszPPId);

    HRESULT GetCursorCount(
        [out] ULONG *pcCurs);

    HRESULT GetCursor(
        [in] ULONG iCur,
        [out] ITabletCursor **ppCur);
};   
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                              |
| 程式庫<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

