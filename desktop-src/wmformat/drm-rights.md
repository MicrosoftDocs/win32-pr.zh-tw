---
title: DRM_Rights
description: '[DRM \_ 許可權] 屬性會指定應用程式在下一次嘗試開啟受保護的檔案時所需的許可權。'
ms.assetid: fbf62e8d-069e-427b-9093-6c579cdaa96a
keywords:
- DRM_Rights windows Media 格式
topic_type:
- apiref
api_name:
- DRM_Rights
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 542e511c11111bb2698d9c936a1f0973a2145c9b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023022"
---
# <a name="drm_rights"></a>DRM \_ 許可權

[ **DRM \_ 許可權** ] 屬性會指定應用程式在下一次嘗試開啟受保護的檔案時所需的許可權。

## <a name="global-constant"></a>全域常數

g \_ wszWMDRM \_ 許可權

## <a name="data-type"></a>資料類型

**WMT \_ 類型 \_ 字串**

## <a name="remarks"></a>備註

這是讀寫屬性，會使用 [**IWMDRMReader：： GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) 抓取，並使用 [**IWMDRMReader：： SetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-setdrmproperty) 或 [**IWMDRMWriter：： SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute)來設定。

下表列出支援的許可權。



| Right                                           | 字串常值      | Description                                                                                                                                                                                                          |
|-------------------------------------------------|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| g \_ wszWMDRM \_ 右 \_ 備份                      | 備份            | 備份授權的許可權。                                                                                                                                                                                        |
| g \_ wszWMDRM \_ RIGHT \_ 協同作業 \_ 播放         | "CollaborativePlay" | 在共同作業播放清單中播放檔案的許可權。                                                                                                                                                          |
| g \_ wszWMDRM \_ RIGHT \_ COPY                        | "Copy"              | 將檔案複製到裝置的許可權。 此許可權會取代較舊的複製許可權 (g \_ wszWMDRM \_ right \_ copy \_ 至 \_ CD、g \_ wszWMDRM \_ right \_ copy \_ 至 \_ 非 \_ SDMI \_ 裝置，以及 g \_ wszWMDRM \_ right \_ 複製 \_ 到 \_ SDMI \_ 裝置) 。 |
| g \_ wszWMDRM \_ RIGHT \_ 複製 \_ 到 \_ CD                | "Print. redbook"     | 將檔案複製到 CD (的紅色書籍格式) 的許可權。在 Windows Media DRM 10 中，此許可權由 g \_ wszWMDRM \_ right COPY 取代 \_ 。<br/>                                                                             |
| g \_ wszWMDRM \_ RIGHT \_ COPY \_ 至 \_ 非 \_ SDMI \_ 裝置 | "Transfer. NONSDMI"  | 將檔案複製到非 SDMI 裝置的許可權。在 Windows Media DRM 10 中，此許可權由 g \_ wszWMDRM \_ right COPY 取代 \_ 。<br/>                                                                                  |
| g \_ wszWMDRM \_ RIGHT \_ 複製 \_ 到 \_ SDMI \_ 裝置      | "Transfer. SDMI"     | 將檔案複製到符合 SDMI 規範之裝置的許可權。在 Windows Media DRM 10 中，此許可權由 g \_ wszWMDRM \_ right COPY 取代 \_ 。<br/>                                                                           |
| g \_ wszWMDRM \_ 右 \_ 播放                    | 發出              | 播放媒體檔案的許可權。                                                                                                                                                                                        |



 

此屬性包含一或多個以分號分隔之許可權的寬字元字串，例如： L "播放;份CollaborativePlay".

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DRM 屬性**](drm-properties.md)
</dt> </dl>

 

 





