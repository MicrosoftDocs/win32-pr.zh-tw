---
description: 本節提供直接操作常數的參考規格。
ms.assetid: 41A828F5-4AE3-4073-89EB-CC1279B9ECED
title: 直接操作常數
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 5040191f22e92dcfb8c2ca26edd4080cd4cbb2be
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106991792"
---
# <a name="direct-manipulation-constants"></a>直接操作常數

本節提供 [直接操作](direct-manipulation-portal.md) 常數的參考規格。

| 常數/值                                                                                                                                                                                                                                                                         | Description                                                                                    |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| <span id="DIRECTMANIPULATION_KEYBOARDFOCUS"></span><span id="directmanipulation_keyboardfocus"></span><dl> <dt>**DIRECTMANIPULATION \_KEYBOARDFOCUS**</dt> <dt>0xFFFFFFFE</dt> </dl> | 指定虛擬指標識別碼，以透過鍵盤輸入來模擬觸控連絡人。<br/> |
| <span id="DIRECTMANIPULATION_MOUSEFOCUS"></span><span id="directmanipulation_mousefocus"></span><dl> <dt>**DIRECTMANIPULATION \_MOUSEFOCUS**</dt> <dt>0xFFFFFFFD</dt> </dl>          | 指定透過滑鼠輸入模擬觸控連絡人的虛擬指標識別碼。<br/>    |
| <span id="DIRECTMANIPULATION_MINIMUM_ZOOM"></span><span id="directmanipulation_minimum_zoom"></span><dl> <dt>**DIRECTMANIPULATION \_最小 \_ 縮放**</dt> <dt>0.1</dt> </dl>          | 指定10% 允許的最小縮放界限。<br/>                               |

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                              |
| Idl<br/>                      | <dl> <dt>DirectManipulation .idl</dt> </dl> |

## <a name="see-also"></a>另請參閱

[直接操作參考](direct-manipulation-reference.md)
