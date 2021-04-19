---
description: 表示簽署者物件的集合。
ms.assetid: 72e86acd-eb87-4eff-bd4e-327630ebbfc4
title: 簽署者物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 75eba0ecb2592bf7efc27ecdd63288179e306651
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990035"
---
# <a name="signers-object"></a>簽署者物件

\[**簽署** 者物件可在 [需求] 區段中指定的作業系統中使用。 相反地，請使用 CmsSigner 物件的集合。 For more information, see the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]

**簽署** 者物件代表 [**簽署者**](signer.md)物件的集合。

## <a name="when-to-use"></a>使用時機

**簽署** 者物件是用來執行下列工作：

-   取得集合中的憑證數目。
-   從集合中取出特定的 **簽署** 者物件。
-   逐一查看集合。

## <a name="members"></a>成員

**簽署** 者物件有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**簽署** 者物件具有這些屬性。



| 屬性                                        | 存取類型          | Description                                                                                                                                                                                                                     |
|:------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](signers-newenum.md)<br/> | 唯讀<br/> | 在可以用來列舉集合的物件上，抓取 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) 介面。 這個屬性會在 Visual Basic Scripting Edition (VBScript) 中隱藏。<br/> |
| [**計數**](signers-count.md)<br/>       | 唯讀<br/> | 集合中的 [**簽署者**](signer.md) 物件數目。<br/>                                                                                                                                                        |
| [**項目**](signers-item.md)<br/>         | 唯讀<br/> | 抓取代表索引簽署者的 [**簽署者**](signer.md) 物件。 這是預設屬性。<br/>                                                                                                      |



 

## <a name="remarks"></a>備註

無法建立 **簽署** 者物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**加密物件**](cryptography-objects.md)
</dt> </dl>

 

 
