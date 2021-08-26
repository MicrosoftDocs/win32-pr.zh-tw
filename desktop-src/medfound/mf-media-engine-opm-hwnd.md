---
description: 指定媒體引擎將輸出保護管理員套用 (OPM) 保護的視窗。
ms.assetid: E5271D72-FE16-4D28-9BBA-1440C7CE0921
title: 'MF_MEDIA_ENGINE_OPM_HWND 屬性 (Mfmediaengine) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e1079e7b9503c73ea678e4f9fd3642ec94fe43a1326e6f33a635f81d1bc1a64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013068"
---
# <a name="mf_media_engine_opm_hwnd-attribute"></a>MF \_ 媒體 \_ 引擎 \_ OPM \_ HWND 屬性

指定媒體引擎將 [輸出保護管理員](output-protection-manager.md) 套用 (OPM) 保護的視窗。

## <a name="data-type"></a>資料類型

**HWND** 儲存為 **UINT64**

## <a name="remarks"></a>備註

這個屬性會與 [**IMFMediaEngineClassFactory：： CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) 方法搭配使用，以初始化 Media Engine。

若要針對影片播放啟用 OPM 保護，應用程式必須執行下列其中一項動作：

-   建立媒體引擎時，請設定 [MF \_ media \_ ENGINE \_ 播放 \_ HWND](mf-media-engine-playback-hwnd.md) 屬性。
-   建立媒體引擎時，請設定 MF \_ media \_ ENGINE \_ OPM \_ HWND 屬性。
-   在建立媒體引擎之後，但在顯示受保護的內容之前，請在任何時間點呼叫 [**IMFMediaEngineProtectedContent：： SetOPMWindow**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setopmwindow) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[桌面應用程式 \| UWP 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows Server 2012 \[桌面應用程式 \| UWP 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Mfmediaengine。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[媒體引擎屬性](media-engine-attributes.md)
</dt> </dl>

 

 




