---
description: 值，指出畫面格來源所提供的感應器類型，例如色彩、紅外線或深度。
ms.assetid: F327B9E9-C01C-4F5B-9A26-6404ECD7F27F
title: 'MF_MT_FRAMESOURCE_TYPES 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4475d66aea245ac9295a7996da2c37cabdb9627
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983395"
---
# <a name="mf_mt_framesource_types-attribute"></a>MF \_ MT \_ FRAMESOURCE \_ 類型屬性

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

值，指出畫面格來源所提供的感應器類型，例如色彩、紅外線或深度。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

此值應該是 [**\_ MFFrameSourceTypes**](/previous-versions/windows/desktop/legacy/mt846679(v=vs.85))列舉的成員。 為了回溯相容性，在媒體類型上未定義此屬性時，會假設為 **\_ MFFrameSourceTyes：： Color**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server，版本 1709 \[ 桌面應用程式\]<br/>                      |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



 

 
