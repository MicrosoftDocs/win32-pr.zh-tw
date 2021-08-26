---
description: 定義輸出保護管理員 (OPM) 的狀態。
ms.assetid: 7C4D88F6-369B-4364-90C4-6D0F8DD1523B
title: MF_MEDIA_ENGINE_OPM_STATUS 列舉
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MEDIA_ENGINE_OPM_STATUS
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: 98efb0054402f8bf019e91d639f16322a1378a23dfeee76cd31daea9d12bf6fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013038"
---
# <a name="mf_media_engine_opm_status-enumeration"></a>MF \_ 媒體 \_ 引擎 \_ OPM \_ 狀態列舉

定義 [輸出保護管理員](output-protection-manager.md) (OPM) 的狀態。

## <a name="syntax"></a>Syntax


```C++
typedef enum _MF_MEDIA_ENGINE_OPM_STATUS { 
  MF_MEDIA_ENGINE_OPM_NOT_REQUESTED           =  0,
  MF_MEDIA_ENGINE_OPM_ESTABLISHED             = 1,
  MF_MEDIA_ENGINE_OPM_FAILED_VM               = 2,
  MF_MEDIA_ENGINE_OPM_FAILED_BDA              = 3,
  MF_MEDIA_ENGINE_OPM_FAILED_UNSIGNED_DRIVER  = 4,
  MF_MEDIA_ENGINE_OPM_FAILED                  = 5
} MF_MEDIA_ENGINE_OPM_STATUS;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="MF_MEDIA_ENGINE_OPM_NOT_REQUESTED"></span><span id="mf_media_engine_opm_not_requested"></span>**\_ \_ \_ \_ 未要求 MF 媒體引擎 \_ OPM**
</dt> <dd>

預設狀態。 當內容未受保護時，用來傳回正確的狀態。

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_ESTABLISHED"></span><span id="mf_media_engine_opm_established"></span>**已 \_ 建立 MF 媒體 \_ 引擎 \_ OPM \_**
</dt> <dd>

已成功建立 OPM。

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_FAILED_VM"></span><span id="mf_media_engine_opm_failed_vm"></span>**MF \_ 媒體 \_ 引擎 \_ OPM \_ 失敗的 \_ VM**
</dt> <dd>

OPM 失敗，因為在虛擬 (VM) 中執行。

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_FAILED_BDA"></span><span id="mf_media_engine_opm_failed_bda"></span>**MF \_ 媒體 \_ 引擎 \_ OPM \_ 失敗 \_ BDA**
</dt> <dd>

OPM 失敗，因為沒有圖形驅動程式，且系統正在使用基本的顯示器介面卡 (BDA) 。

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_FAILED_UNSIGNED_DRIVER"></span><span id="mf_media_engine_opm_failed_unsigned_driver"></span>**MF \_ 媒體 \_ 引擎 \_ OPM \_ 失敗的 \_ 未簽署 \_ 驅動程式**
</dt> <dd>

OPM 失敗，因為圖形驅動程式未經過 PE 簽署，因此切換回變形。

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_FAILED"></span><span id="mf_media_engine_opm_failed"></span>**MF \_ 媒體 \_ 引擎 \_ OPM \_ 失敗**
</dt> <dd>

OPM 因其他原因而失敗。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[僅限桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | Windows Server 2012\[僅限 R2 desktop 應用程式\]<br/>                                      |
| IDL<br/>                      | <dl> <dt>Mfmediaengine .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎列舉](media-foundation-enumerations.md)
</dt> </dl>

 

 




