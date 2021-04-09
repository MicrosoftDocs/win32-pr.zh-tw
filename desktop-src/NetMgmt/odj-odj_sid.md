---
title: ODJ_SID
description: ODJ_SID IDL 定義
ms.assetid: 1d06f725-6cd4-42cf-b171-c78a095690cb
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: dd51f2e8a54eaf5be566e5a25f013ca1d87b9341
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/14/2020
ms.locfileid: "104024283"
---
# <a name="odj_sid-structure"></a>ODJ_SID 結構

包含 (SID) 的安全識別碼。

## <a name="syntax"></a>語法

```C++
typedef struct _ODJ_SID
{
    UCHAR Revision;
    UCHAR SubAuthorityCount;
    SID_IDENTIFIER_AUTHORITY IdentifierAuthority;
    [size_is(SubAuthorityCount)] ULONG SubAuthority[*];
}   ODJ_SID, *PODJ_SID;
```

## <a name="members"></a>成員

### <a name="revision"></a>修訂版

必須設定為 SID 修訂。

### <a name="subauthoritycount"></a>SubAuthorityCount

必須設定為 SubAuthority 中的元素數目。

### <a name="identifierauthority"></a>IdentifierAuthority

必須設定為 SID 授權單位識別碼。

### <a name="subauthority"></a>SubAuthority

必須包含 SID 子授權陣列。

## <a name="see-also"></a>另請參閱

[**離線網域加入 IDL 定義**](odj-idl.md)

[**ODJ \_ SID \_ 識別碼 \_ 授權單位**](odj-sid_identifier_authority.md)
