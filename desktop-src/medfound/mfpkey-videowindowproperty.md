---
description: 指定可符合模型緩衝區的內容數量（以毫秒為單位）。
ms.assetid: da959bef-1e87-4638-9a77-4135c31a3d27
title: 'MFPKEY_VIDEOWINDOW 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f33d10b3a589ef3bcfc945b2c3404c7b02cb7121
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512637"
---
# <a name="mfpkey_videowindow-property"></a>MFPKEY \_ VIDEOWINDOW 屬性

指定可符合模型緩衝區的內容數量（以毫秒為單位）。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMVCVideoWIndow

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="default-value"></a>預設值

3000

## <a name="remarks"></a>備註

緩衝區視窗是編解碼器速率控制項中所使用的其中一個「有漏洞 bucket」模型參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[設定影片編碼](configuringvideoencoding.md)
</dt> <dt>

[有漏洞 Bucket 緩衝區模型](the-leaky-bucket-buffer-model.md)
</dt> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 




