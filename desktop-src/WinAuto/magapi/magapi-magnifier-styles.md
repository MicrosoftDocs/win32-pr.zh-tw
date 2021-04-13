---
title: 放大鏡樣式
description: 本主題說明與 [放大鏡] 控制項搭配使用的樣式。
ms.assetid: B3C575AC-B8D3-40CF-AF09-BAC73E6C7B45
topic_type:
- apiref
api_name:
- MS_CLIPAROUNDCURSOR
- MS_INVERTCOLORS
- MS_SHOWMAGNIFIEDCURSOR
api_location:
- Magnification.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 212e079a59db9a85b6d232d1c11ac9f46eceb314
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384693"
---
# <a name="magnifier-styles"></a>放大鏡樣式

本主題說明與 [放大鏡] 控制項搭配使用的樣式。 若要建立放大鏡控制項，請使用 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) 函式並指定 WC_MAGNIFIER 視窗類別，以及下列放大鏡樣式的組合。

| 需求 | 值 |
|:---|:---|
| MS_CLIPAROUNDCURSOR 0x0002L | 剪住系統游標周圍的 [放大鏡] 視窗區域。 此樣式可讓使用者查看位於放大鏡視窗後方的螢幕內容。 |
| MS_INVERTCOLORS 0x0004L | 使用反向色彩顯示放大的螢幕內容。 |
| MS_SHOWMAGNIFIEDCURSOR 0x0001L | 顯示放大的系統游標以及放大的螢幕內容。 |

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>放大。h</dt> </dl> |

## <a name="see-also"></a>另請參閱

[常數](entry-magapi-constants.md)
