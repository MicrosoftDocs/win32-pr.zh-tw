---
description: 啟用影片管線中的靜態優化。
ms.assetid: 62fb3f0f-ab1f-4c61-8e7f-62908b947788
title: 'MF_TOPOLOGY_STATIC_PLAYBACK_OPTIMIZATIONS 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f01b22e5b7e972e9d1eb453f317e8db6a902e994e83d075cd791d9261aa6ed09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117691240"
---
# <a name="mf_topology_static_playback_optimizations-attribute"></a>MF \_ 拓撲 \_ 靜態 \_ 播放 \_ 優化屬性

啟用影片管線中的靜態優化。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="applies-to"></a>適用於

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>備註

請先設定這個屬性，然後再載入拓撲。 如果屬性為 **TRUE**，拓撲載入器會嘗試在播放開始之前將管線優化。

如果設定此屬性，您也應該設定下列屬性：

-   [MF \_ 拓撲 \_ 播放 \_ 畫面播放速率](mf-topology-playback-framerate.md)
-   [MF \_ 拓撲 \_ 播放 \_ 最大 \_ 亮度](mf-topology-playback-max-dims.md)

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="examples"></a>範例


```C++
HRESULT SetPlaybackOptimizations(IMFTopology *pTopology, HWND hwnd)
{
    HRESULT hr = pTopology->SetUINT32(
        MF_TOPOLOGY_STATIC_PLAYBACK_OPTIMIZATIONS, TRUE);

    if (FAILED(hr))
    {
        return hr;
    }

    HMONITOR hCurrentMon = MonitorFromWindow(hwnd, MONITOR_DEFAULTTOPRIMARY);

    if (hCurrentMon)
    {
        MONITORINFO MonitorInfo = {0};
        MonitorInfo.cbSize = sizeof(MONITORINFO);

        BOOL fSucceeded = GetMonitorInfo(hCurrentMon, &MonitorInfo);

        if (fSucceeded )
        {
            const RECT& rcMonitor = MonitorInfo.rcMonitor;

            LONG width = rcMonitor.right - rcMonitor.left;
            LONG height = rcMonitor.bottom - rcMonitor.top;

            hr = MFSetAttributeSize(
                pTopology, 
                MF_TOPOLOGY_PLAYBACK_MAX_DIMS, 
                (UINT32)width, (UINT32)height
                );

            if (FAILED(hr))
            {
                goto done;
            }

            HDC hdc = GetDC(hwnd);

            hr = MFSetAttributeRatio(
                pTopology,
                MF_TOPOLOGY_PLAYBACK_FRAMERATE,
                GetDeviceCaps(hdc, VREFRESH), 1
                );

            ReleaseDC(hwnd, hdc);
        }
    }
done:
    return hr;
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                            |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[拓撲屬性](topology-attributes.md)
</dt> <dt>

[影片品質管制](video-quality-management.md)
</dt> </dl>

 

 




