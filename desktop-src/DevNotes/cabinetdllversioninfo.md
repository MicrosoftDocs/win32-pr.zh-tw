---
description: CABINETDLLVERSIONINFO 包含 Cabinet.dll 的版本資訊。
ms.assetid: 1dc6962c-3087-4f56-8b65-fbf55e17eeb6
title: CABINETDLLVERSIONINFO 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CABINETDLLVERSIONINFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: b6dfcd68f1bc684554d45feb13b9976465b70efa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847236"
---
# <a name="cabinetdllversioninfo-structure"></a>CABINETDLLVERSIONINFO 結構

\[只有在使用不支援的 **DllGetVersion** 函數時，此結構才會包含所需的資訊。 本檔僅供參考之用。\]

**CABINETDLLVERSIONINFO** 包含 Cabinet.dll 的版本資訊。

## <a name="syntax"></a>語法


```C++
typedef struct {
  DWORD cbStruct;
  DWORD dwReserved1;
  DWORD dwReserved2;
  DWORD dwFileVersionMS;
  DWORD dwFileVersionLS;
} CABINETDLLVERSIONINFO, *PCABINETDLLVERSIONINFO;
```



## <a name="members"></a>成員

<dl> <dt>

**cbStruct**
</dt> <dd>

此結構的大小（以位元組為單位）。

</dd> <dt>

**dwReserved1**
</dt> <dd>

保留的。

</dd> <dt>

**dwReserved2**
</dt> <dd>

保留的。

</dd> <dt>

**dwFileVersionMS**
</dt> <dd>

包含版本資訊的最高有效位。 Bits 0-15 包含次要版本，而 bits 16-31 包含主要版本。

</dd> <dt>

**dwFileVersionLS**
</dt> <dd>

包含版本資訊的最小有效位。 Bits 0-15 包含修訂編號，而 bits 16-31 包含組建編號。

</dd> </dl>

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DllGetVersion**](dllgetversion.md)
</dt> </dl>

 

 



