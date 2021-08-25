---
description: 本節中的主題提供指標裝置輸入堆疊結構的參考規格。
ms.assetid: 33DCB172-8D95-4205-AE2E-ADD7F3BF988A
title: '結構 (指標裝置輸入) '
ms.topic: article
ms.date: 02/05/2020
ms.openlocfilehash: 042e1582d9c01cc6779ad672fb4935d288d29d8f442011d88e2b967b6adcf50a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830268"
---
# <a name="pointer-device-input-stack-structures"></a>指標裝置輸入堆疊結構

本節中的主題提供 [指標裝置輸入堆疊](pointer-device-stack-portal.md) 結構的參考規格。

## <a name="in-this-section"></a>本節內容

| 主題 | 描述 |
|---|---|
| [**POINTER_DEVICE_CURSOR_INFO**](/windows/win32/api/winuser/ns-winuser-pointer_device_cursor_info)<br/> | 包含指標裝置的資料指標識別碼對應。<br/> |
| [**POINTER_DEVICE_INFO**](/windows/win32/api/winuser/ns-winuser-pointer_device_info)<br/> | 包含指標裝置的相關資訊。 這些結構的陣列是從 [**GetPointerDevices**](/windows/win32/api/winuser/nf-winuser-getpointerdevices) 函式傳回。 從呼叫 [**GetPointerDevice**](/windows/win32/api/winuser/nf-winuser-getpointerdevice) 函數時，會傳回單一結構。 <br/> |
| [**POINTER_DEVICE_PROPERTY**](/windows/win32/api/winuser/ns-winuser-pointer_device_property)<br/> | 包含裝置屬性 (人體介面裝置 (HID) 對應至的隱藏專案) 的全域專案。<br/> |

## <a name="related-topics"></a>相關主題

[指標裝置輸入堆疊參考](unified-input-stack-reference.md)
