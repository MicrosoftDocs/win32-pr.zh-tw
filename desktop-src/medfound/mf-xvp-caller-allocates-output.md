---
description: 指定呼叫端是否要配置用於輸出的材質。
ms.assetid: CAB41B22-AD96-4932-9686-66474CB26C38
title: 'MF_XVP_CALLER_ALLOCATES_OUTPUT 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: def1b1d138c031393e1a1b1a3832c1ad6d066306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512257"
---
# <a name="mf_xvp_caller_allocates_output-attribute"></a>MF \_ XVP \_ 呼叫端配置 \_ \_ 輸出屬性

指定呼叫端是否要配置用於輸出的材質。

## <a name="data-type"></a>資料類型

**BOOL** 儲存為 **UINT32**

## <a name="remarks"></a>備註

如果此屬性為 **TRUE**，則影片處理器預期輸出材質會由呼叫端配置，即使在 DirectX video 加速作業 (DXVA) 模式下運作。 如果這個屬性為 **FALSE**，則在 DXVA 模式中操作時，影片處理器會配置輸出紋理，如果提供者提供的輸出紋理，則會失敗。

若要設定此屬性：

1.  在視頻處理器上呼叫 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) 。
2.  呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

開始串流之前，請設定屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2016 \[ desktop 應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Mfidl .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




