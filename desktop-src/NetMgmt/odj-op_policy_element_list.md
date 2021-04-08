---
title: OP_POLICY_ELEMENT_LIST
description: OP_POLICY_ELEMENT_LIST IDL 定義
ms.assetid: 1eebbdd2-655b-4bd3-938c-6bc687ffe7bb
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 3c46e7208e6c142b9f58a7704be9bd3461c845b2
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/14/2020
ms.locfileid: "103684207"
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
