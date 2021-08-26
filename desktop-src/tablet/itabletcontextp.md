---
description: 表示 tablet 內容。
ms.assetid: d518c42d-c2f6-4776-bea5-fecdfe48e260
title: ITabletCoNtextP 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: da5c26a0a9d7d080a9787fef0b7ba2fdb919e473fd66c989fca478c4ac7d0ac3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883518"
---
# <a name="itabletcontextp-interface"></a>ITabletCoNtextP 介面

表示 tablet 內容。

## <a name="members"></a>成員

**ITabletCoNtextP** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **ITabletCoNtextP** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ITabletCoNtextP** 介面具有這些方法。



| 方法                                                                                           | 描述                                                                     |
|:-------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------|
| [**IsTopMostHook**](itabletcontextp-istopmosthook.md)                                           | 指出 tablet 內容是否在最上層的掛勾中。<br/>             |
| [**重疊**](itabletcontextp-overlap.md)                                                       | 將 tablet 內容移至輸入佇列的前端或背面。<br/>      |
| [**TrackInputRect**](itabletcontextp-trackinputrect.md)                                         | 將 tablet 數位板更新為視窗位置對應座標。<br/> |
| [**UseNamedSharedMemoryCommunications**](itabletcontextp-usenamedsharedmemorycommunications.md) | 提供 tablet 執行緒之間共用記憶體的存取。<br/>             |
| [**UseSharedMemoryCommunications**](itabletcontextp-usesharedmemorycommunications.md)           | 提供 tablet 執行緒之間共用記憶體的存取。<br/>             |



 

## <a name="remarks"></a>備註

開發人員不應使用此介面。

[**UseNamedSharedMemoryCommunications**](itabletcontextp-usenamedsharedmemorycommunications.md)僅適用于 Windows Vista 和更新版本。

下列程式碼說明如何定義 **ITabletCoNtextP** 介面。

``` syntax
[
    object,
    uuid(22F74D0A-694F-4f47-A5CE-AE08A6409AC8),
    pointer_default(unique)
]
interface ITabletContextP : ITabletContext
{

    HRESULT Overlap([in] BOOL bTop, [out] DWORD *pdwtcid);

    HRESULT GetType([out] CONTEXT_TYPE *pct);

    HRESULT TrackInputRect([out] RECT *prcInput);

    HRESULT IsTopMostHook();

    HRESULT GetEventSink(
        [out] ITabletEventSink **ppSink);

    HRESULT UseSharedMemoryCommunications(
        [in]  DWORD pid,
        [out] DWORD *phEventMoreData,
        [out] DWORD *phEventClientReady,
        [out] DWORD *phMutexAccess,
        [out] DWORD *phFileMapping);

    HRESULT UseNamedSharedMemoryCommunications(
        [in] DWORD pid,
        [in, string] LPCTSTR szSid,
        [in, string] LPCTSTR sdIlSid,
        [out] DWORD *pdwEventMoreDataId,
        [out] DWORD *pdwEventClientReadyId,
        [out] DWORD *pdwMutexAccessId,
        [out] DWORD *pdwFileMappingId);
};
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                              |
| 程式庫<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

