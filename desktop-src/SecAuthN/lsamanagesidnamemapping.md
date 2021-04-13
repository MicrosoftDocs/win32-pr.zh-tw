---
UID: ''
title: LsaManageSidNameMapping 函式
description: 從向 LSA 查閱服務註冊的對應集中，加入或移除 SID/名稱對應。
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: ''
ms.topic: reference
req.header: Ntsecapi.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Secur32.lib
req.dll:
- Advapi32.dll
- API-MS-Win-DownLevel-AdvAPI32-l4-1-0.dll
- API-MS-Win-security-lsalookup-l2-1-1.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location: ''
api_name:
- LsaManageSidNameMapping
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: fc0065c3964718d690149693f3c71ec4e9f676ec
ms.sourcegitcommit: 382c7259008374408368c173e0027fb641c848fe
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/22/2020
ms.locfileid: "104314493"
---
# <a name="lsamanagesidnamemapping-function"></a>LsaManageSidNameMapping 函式

## <a name="description"></a>Description

**LsaManageSidNameMapping** 函式會從向 LSA 查閱服務註冊的對應集中，新增或移除 SID/名稱對應。

```cpp
void WINAPI LsaManageSidNameMapping(
  _In_  LSA_SID_NAME_MAPPING_OPERATION_TYPE    OpType,
  _In_  PLSA_SID_NAME_MAPPING_OPERATION_INPUT  OpInput,
  _Out_ PLSA_SID_NAME_MAPPING_OPERATION_OUTPUT *OpOutput
);
```

## <a name="parameters"></a>參數

### <a name="optype-in"></a>OpType [in]

指出是否呼叫這個函式來新增或移除 SID/名稱對應。

### <a name="opinput-in"></a>OpInput [in]

指出要在此作業期間使用的網域、帳戶和 SID 值。 您也可以在此結構內設定其他旗標。

### <a name="opoutput-out"></a>OpOutput [out]

包含表示作業成功或失敗的 [LSA_SID_NAME_MAPPING_OPERATION_ERROR](/previous-versions/windows/desktop/legacy/dn280707(v=vs.85)) 值。

| 值 | 意義 |
|-------|---------|
| 「成功」 | 作業已完成，未發生錯誤。 |
| **NonMappingError** | 發生與 SID 名稱對應無關的錯誤。 |
| **NameCollision** | 因名稱衝突而導致作業失敗。 |
| **SidCollision** | 因 SID 衝突而導致作業失敗。 |
| **DomainNotFound** | 找不到對應的網域。 |
| **DomainSidPrefixMismatch** | 提供的 SID 沒有正確的網域前置詞。 |
| **MappingNotFound** | 在快取中找不到對應。 |

## <a name="returns"></a>傳回

如果成功插入對應，則傳回值為 STATUS_SUCCESS。
否則，如果函式因為 SID 或名稱衝突而失敗，則會傳回 STATUS_INVALID_PARAMETER 錯誤。

## <a name="remarks"></a>備註

## <a name="see-also"></a>另請參閱
