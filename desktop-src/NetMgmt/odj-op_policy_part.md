---
title: OP_POLICY_PART
description: OP_POLICY_PART IDL 定義
ms.assetid: 3988b298-b21d-4476-bfa5-ac606bcbd6c8
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 8ad479c2e24d8c38e87a2100658be2afcf37d70d321e99433e3b05a3af35fa60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911478"
---
# <a name="op_policy_part-structure"></a>OP_POLICY_PART 結構

包含 OP_POLICY_ELEMENT_LIST 結構的陣列。

## <a name="syntax"></a>語法

```C++
typedef struct _OP_POLICY_PART
{
    ULONG                                       cElementLists;
    [size_is(cElementLists)]
                        POP_POLICY_ELEMENT_LIST pElementLists;
    OP_BLOB                                     Extension;
} OP_POLICY_PART, *POP_POLICY_PART;
```

## <a name="members"></a>成員

### <a name="celementlists"></a>cElementLists

包含 pElementLists 中的元素數目。

### <a name="pelementlists"></a>pElementLists

包含 OP_POLICY_ELEMENT_LIST 結構的陣列。

### <a name="extension"></a>延伸模組

保留供日後使用，且必須包含所有的零。

## <a name="see-also"></a>另請參閱

[**離線網域加入 IDL 定義**](odj-idl.md)

[**OP \_ 原則 \_ 元素 \_ 清單**](odj-op_policy_element_list.md)
