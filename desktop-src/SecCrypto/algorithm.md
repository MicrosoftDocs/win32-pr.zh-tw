---
description: 指定用於簽署、封套和加密作業的演算法。
ms.assetid: 9a3071a3-e62d-43d3-acd7-0685592c78b4
title: '演算法物件 (Capicom. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f564efe9df3122951969a45443d58ace60e9db30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994572"
---
# <a name="algorithm-object"></a>演算法物件

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista、Windows XP。 相反地，請使用 [**AlgorithmIdentifier 類別**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

**演算法** 物件指定用於簽署、封套和加密作業的演算法。

## <a name="when-to-use"></a>使用時機

**演算法** 物件是用來執行下列工作：

-   設定或取出要使用的演算法。
-   設定或取出金鑰長度。

> [!Note]  
> CAPICOM 嘗試使用系統預設密碼編譯服務提供者 (CSP) 。 如果該 CSP 無法提供所要求的演算法或金鑰長度，則 CAPICOM 會搜尋可用的 Microsoft 提供的 CSP，以處理要求的演算法和金鑰長度（依此可用性順序）： Microsoft 增強型密碼編譯提供者、Microsoft 強式密碼編譯提供者、Microsoft 基礎密碼編譯提供者。

 

## <a name="members"></a>成員

**演算法** 物件有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**演算法** 物件具有這些屬性。



| 屬性                                            | 存取類型           | Description                                                                                                                       |
|:----------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**KeyLength**](algorithm-keylength.md)<br/> | 讀取/寫入<br/> | 設定或抓取索引鍵的長度。<br/>                                                                               |
| [**Name**](algorithm-name.md)<br/>           | 讀取/寫入<br/> | 設定或抓取用於簽署、封套和加密作業的演算法。 這是預設屬性。<br/> |



 

## <a name="remarks"></a>備註

無法建立 **演算法** 物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| 標頭<br/>                | <dl> <dt>Capicom</dt> </dl>   |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**加密物件**](cryptography-objects.md)
</dt> </dl>

 

 
