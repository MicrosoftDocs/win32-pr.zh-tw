---
description: 定義用於 MF \_ 視頻處理器演算法的視頻處理器演算法 \_ \_ 。
ms.assetid: 3BB0836E-39E6-40FA-9BA0-C986EB587CF1
title: MF_VIDEO_PROCESSOR_ALGORITHM_TYPE 列舉
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_VIDEO_PROCESSOR_ALGORITHM_TYPE
api_type:
- HeaderDef
api_location:
- mfidl.h
ms.openlocfilehash: 885c3e9c34fa787a6877fd37eef81f470be395225594b90b2f5516a8e773eb88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244136"
---
# <a name="mf_video_processor_algorithm_type-enumeration"></a>MF \_ 視頻 \_ 處理器 \_ 演算法 \_ 類型列舉

定義用於 [MF \_ 視頻 \_ 處理器 \_ 演算法](mf-video-processor-algorithm.md)的視頻處理器演算法。

## <a name="syntax"></a>Syntax


```C++
typedef enum _MF_VIDEO_PROCESSOR_ALGORITHM_TYPE { 
  MF_VIDEO_PROCESSOR_ALGORITHM_DEFAULT      = 0,
  MF_VIDEO_PROCESSOR_ALGORITHM_MRF_CRF_444  = 1
} MF_VIDEO_PROCESSOR_ALGORITHM_TYPE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="MF_VIDEO_PROCESSOR_ALGORITHM_DEFAULT"></span><span id="mf_video_processor_algorithm_default"></span>**MF \_ 視頻 \_ 處理器 \_ 演算法 \_ 預設**
</dt> <dd>

預設模式優先于品質與速度的平衡

</dd> <dt>

<span id="MF_VIDEO_PROCESSOR_ALGORITHM_MRF_CRF_444"></span><span id="mf_video_processor_algorithm_mrf_crf_444"></span>**MF \_ 視頻 \_ 處理器 \_ 演算法 \_ .mrf \_ CRF \_ 444**
</dt> <dd>

影片處理器一律會在內部處理 AYUV，並使用高品質的篩選。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[僅限桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows Server 2012\[僅限 R2 desktop 應用程式\]<br/>                              |
| Idl<br/>                      | <dl> <dt>Mfidl .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎列舉](media-foundation-enumerations.md)
</dt> </dl>

 

 




