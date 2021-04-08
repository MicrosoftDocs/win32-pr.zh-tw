---
title: _allmul 常式
description: 將兩個 LONGLONG 或 ULONGLONG 整數相乘。
ms.assetid: na
ms.topic: reference
ms.date: 04/29/2019
ms.keywords: _allmul, ntoskrnl.exe!_allmul
topic_type:
- APIRef
api_type:
- DllExport
api_location:
- ntoskrnl.exe
api_name:
- _allmul
targetos: Windows
ms.openlocfilehash: a82a4d56ecb657e19b9849d10c9b51521af6c262
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2020
ms.locfileid: "104022955"
---
# <a name="_allmul-routine"></a>\_allmul 常式

將兩個 **LONGLONG** 或 **ULONGLONG** 整數相乘。
例如，若要將兩個 int64 值相乘，編譯器可能會產生對 **\_ allmul** 常式的呼叫。

## <a name="remarks"></a>備註

**\_ Allmul** 常式是 C 編譯器的 helper 常式。
編譯器是否使用 **\_ allmul** 完全取決於優化集。

此常式只適用于 x86 平臺。
