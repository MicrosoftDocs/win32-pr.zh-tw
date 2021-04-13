---
title: OP_PACKAGE_PART
description: OP_PACKAGE_PART IDL 定義
ms.assetid: 8f13aa71-a7b2-41ee-ad1e-4953f49a391a
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 74f299c58b9bf417a94119cd7520b7c0a364f73a
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/14/2020
ms.locfileid: "104186645"
---
# <a name="op_package_part-structure"></a>OP_PACKAGE_PART 結構

定義結構，其中包含 GUID 所識別的資料集。

## <a name="syntax"></a>語法

```C++
typedef struct _OP_PACKAGE_PART
{
    GUID    PartType;
    ULONG   ulFlags;
    OP_BLOB Part;
    OP_BLOB Extension;
} OP_PACKAGE_PART, *POP_PACKAGE_PART;
```

## <a name="members"></a>成員

### <a name="parttype"></a>PartType

識別包含在下表部分的序列化結構：

|PartType|意義|
| --- | --- |
|GUID_JOIN_PROVIDER {631c7621-5289-4321-bc9e-80f843f868c3}|包含序列化的 ODJ_WIN7_BLOB 結構。|
|GUID_JOIN_PROVIDER2 {57BFC56B-52F9-480C-ADCB-91B3F8A82317}|包含序列化的 OP_JOIN_PROV2_PART 結構。|
|GUID_JOIN_PROVIDER3 {FC0CCF25-7FFA-474A-8611-69FFE269645F}|包含序列化的 OP_JOIN_PROV3_PART 結構。|
|GUID_CERT_PROVIDER {9c0971e9-832f-4873-8e87-ef1419d4781e}|包含序列化的 OP_CERT_PART 結構。|
|GUID_POLICY_PROVIDER {68fb602a-0c09-48ce-b75f-07b7bd58f7ec}|包含序列化的 OP_POLICY_PART 結構。|

### <a name="ulflags"></a>ulFlags

必須設定為零或多個下列旗標：

|值|意義|
| --- | --- |
|OPSPI_PACKAGE_PART_ESSENTIAL (0x00000001) |此封裝部分視為必要。 如果取用者無法辨識此封裝部分或無法成功處理，則整體作業必須失敗。|

### <a name="part"></a>部分

包含 OP_BLOB 結構中的序列化結構。 特定結構取決於 PartType。

### <a name="extension"></a>分機

保留供日後使用，且必須設定為全部為零。

## <a name="see-also"></a>另請參閱

[**離線網域加入 IDL 定義**](odj-idl.md)

[**OP \_ BLOB**](odj-op_blob.md)
