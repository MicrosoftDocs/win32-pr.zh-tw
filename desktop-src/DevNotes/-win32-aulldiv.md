---
title: _aulldiv 常式
description: 將兩個 ULONGLONG 整數相除。
ms.assetid: na
ms.topic: reference
ms.date: 04/29/2019
ms.keywords: _aulldiv, ntoskrnl.exe!_aulldiv
topic_type:
- APIRef
api_type:
- DllExport
api_location:
- ntoskrnl.exe
api_name:
- _aulldiv
targetos: Windows
ms.openlocfilehash: 0a37dd5a88d668ed92d79f7bc939119068840741a54cfacb5a15119fcefb774e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538898"
---
# <a name="_aulldiv-routine"></a>\_aulldiv 常式

將兩個 **ULONGLONG** 整數相除。
例如，若要將兩個 uint64 值相除，編譯器可能會產生對 **\_ aulldiv** 常式的呼叫。

## <a name="remarks"></a>備註

**\_ Aulldiv** 常式是 C 編譯器的 helper 常式。
編譯器是否使用 **\_ aulldiv** 完全取決於優化集。

此函式僅適用于 x86 平臺。
