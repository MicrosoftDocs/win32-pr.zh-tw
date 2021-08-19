---
title: OP_POLICY_ELEMENT
description: OP_POLICY_ELEMENT IDL 定義
ms.assetid: 69f6e0e7-3f47-4fee-8a4c-df94093dcffa
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 74e81f09f4d45d42f5e9df585b88051ac1e96e8cd33e4c15807701e61825b43b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117983382"
---
# <a name="op_policy_element-structure"></a>OP_POLICY_ELEMENT 結構

定義登錄機碼和值名稱、類型，以及應該在該金鑰下設定的值。

## <a name="syntax"></a>語法

```C++
typedef struct _OP_POLICY_ELEMENT
{
    [string] wchar_t                *pKeyPath;
    [string] wchar_t                *pValueName;
    ULONG                           ulValueType;
    ULONG                           cbValueData;
    [size_is(cbValueData)]  PBYTE   pValueData;
} OP_POLICY_ELEMENT, *POP_POLICY_ELEMENT;
```

## <a name="members"></a>成員

### <a name="pkeypath"></a>pKeyPath

包含登錄機碼的路徑。

### <a name="pvaluename"></a>pValueName

包含登錄值的名稱。

### <a name="ulvaluetype"></a>ulValueType

包含登錄 [數值型別](../sysinfo/registry-value-types.md)的其中一個值。

### <a name="cbvaluedata"></a>cbValueData

包含 pValueData 的大小（以位元組為單位）。

### <a name="ulvaluetype"></a>ulValueType

包含登錄值的值。

## <a name="see-also"></a>另請參閱

[**離線網域加入 IDL 定義**](odj-idl.md)