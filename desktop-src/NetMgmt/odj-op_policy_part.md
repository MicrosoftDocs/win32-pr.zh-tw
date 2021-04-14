---
title: OP_POLICY_PART
description: OP_POLICY_PART IDL 定義
ms.assetid: 3988b298-b21d-4476-bfa5-ac606bcbd6c8
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: ef0e3b96ce564ed7ff8e2ce0886e33ca474a1cf8
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/14/2020
ms.locfileid: "104383174"
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

### <a name="extension"></a>分機

保留供日後使用，且必須包含所有的零。

## <a name="see-also"></a>另請參閱

[**離線網域加入 IDL 定義**](odj-idl.md)

[**OP \_ 原則 \_ 元素 \_ 清單**](odj-op_policy_element_list.md)
