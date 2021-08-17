---
title: OP_POLICY_ELEMENT_LIST
description: OP_POLICY_ELEMENT_LIST IDL 定義
ms.assetid: 1eebbdd2-655b-4bd3-938c-6bc687ffe7bb
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 1fde1bb1d2794be4fd1bf799282a0257b78ae213453566208ff64bcf7a312654
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796859"
---
# <a name="op_policy_element_list-structure"></a>OP_POLICY_ELEMENT_LIST 結構

定義根登錄機碼，以及要在該機碼下設定的登錄機碼元素陣列。

## <a name="syntax"></a>語法

```C++
typedef struct _OP_POLICY_ELEMENT_LIST
{
    [string] wchar_t                            *pSource;
    ULONG                                       ulRootKeyId;
    ULONG                                       cElements;
    [size_is(cElements)]    POP_POLICY_ELEMENT  pElements;
} OP_POLICY_ELEMENT_LIST, *POP_POLICY_ELEMENT_LIST;
```

## <a name="members"></a>成員

### <a name="psource"></a>pSource

包含所包含之元素來源群組原則檔案的路徑。

### <a name="ulrootkeyid"></a>ulRootKeyId

包含根登錄機碼的識別碼;目前必須設定為 HKEY_LOCAL_MACHINE。

### <a name="celements"></a>cElements

包含 pElements 中的元素數目。

### <a name="pelements"></a>pElements

包含 OP_POLICY_ELEMENT 元素的陣列。

## <a name="see-also"></a>另請參閱

[**離線網域加入 IDL 定義**](odj-idl.md)

[**OP \_ 原則 \_ 元素**](odj-op_policy_element.md)
