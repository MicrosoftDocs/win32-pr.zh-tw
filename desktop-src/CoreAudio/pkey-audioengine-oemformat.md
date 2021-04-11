---
description: PKEY \_ AudioEngine \_ OEMFormat 屬性會指定用來轉譯或捕捉資料流程之裝置的預設格式。 在 .inf 檔案中，OEM 會填入這些值。
ms.assetid: 3a199ecf-642c-491c-a565-f0083783d180
title: 'PKEY_AudioEngine_OEMFormat (Mmdeviceapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be7ed65ae8a7bd717992b13dc7b5517a5725b241
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111312"
---
# <a name="pkey_audioengine_oemformat"></a>PKEY \_ AudioEngine \_ OEMFormat

PKEY \_ AudioEngine \_ OEMFormat 屬性會指定用來轉譯或捕捉資料流程之裝置的預設格式。 在 .inf 檔案中，OEM 會填入這些值。

**PROPVARIANT** 結構的 **vt** 成員會設定為 vt \_ BLOB。

**PROPVARIANT** 結構的 **Blob** 成員是 **blob** 類型的結構，其中包含兩個成員。 成員 **blob。 cbSize** 是一個 **DWORD** ，可指定格式描述中的位元組數目。 成員 **blob. pBlobData** 指向包含格式描述的 **WAVEFORMATEX** 結構。 如需 BLOB 的詳細資訊，請參閱 Windows SDK 檔。 如需 **WAVEFORMATEX** 的詳細資訊，請參閱 Windows DDK 檔。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Mmdeviceapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**音訊端點屬性**](audio-endpoint-properties.md)
</dt> <dt>

[核心音訊屬性](core-audio-properties.md)
</dt> </dl>

 

 




