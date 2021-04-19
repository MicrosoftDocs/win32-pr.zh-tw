---
description: 設定或抓取要簽署的資料。 這是預設屬性。
ms.assetid: 554ca500-403d-4c2a-868e-9e635d0b358e
title: SignedData 內容屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Content
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3c2ac97eeee317b4ec170338f666e5b5d9277861
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998680"
---
# <a name="signeddatacontent-property"></a>SignedData 內容屬性

\[[ **內容** ] 屬性可用於 [需求] 區段中指定的作業系統。 相反地，請使用 [**SignedCms 類別**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

**Content** 屬性會設定或抓取要簽署的資料。 這是預設屬性。

## <a name="syntax"></a>Syntax


```VB
SignedData.Content As String
```



## <a name="property-value"></a>屬性值

要簽署的資料。

## <a name="remarks"></a>備註

這個屬性必須在呼叫 [**Sign**](signeddata-sign.md) 方法之前初始化。 當這個屬性的值是直接或間接重設時，會重設物件的整個 [*狀態*](../secgloss/s-gly.md) ，而且在變更屬性之前與物件相關聯的任何簽章都會遺失。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SignedData**](signeddata.md)
</dt> </dl>

 

 
