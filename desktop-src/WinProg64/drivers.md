---
title: 64位 Windows) 的驅動程式 (程式設計指南
description: 64位版本的 Windows 的設計目的，是為了讓開發人員可以針對其32位和64位應用程式使用單一原始程式碼基底。 在很大的程度上，這也適用于32位和64位 Windows 驅動程式。
ms.assetid: 85d789c9-91dd-4cdc-a10b-c38a455fc940
keywords:
- 驅動程式 64-位 Windows 程式設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cda928bbfc8c7f83e3aeac0bacbaea1e1a46214d9c0785d4675a3042b87fa1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132851"
---
# <a name="drivers-programming-guide-for-64-bit-windows"></a>64位 Windows) 的驅動程式 (程式設計指南

64位版本的 Windows 的設計目的，是為了讓開發人員可以針對其32位和64位應用程式使用單一原始程式碼基底。 在很大的程度上，這也適用于32位和64位 Windows 驅動程式。

但是，32位驅動程式無法在64位的 Windows 上執行，因此必須進行移植。 針對使用者模式應用程式，64位 Windows 包含 WOW64，可讓32位 Windows 應用程式在執行64位 Windows 的系統上執行 (，並) 某些效能降低。 驅動程式沒有對等的轉譯層存在。

如需將驅動程式移植到64位 Windows 的詳細資訊，請參閱 Windows 驅動程式套件 (WDK) 中的[64 位問題](https://msdn.microsoft.com/library/aa489627.aspx)。

 

 




