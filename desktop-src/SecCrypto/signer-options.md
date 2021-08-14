---
description: 設定或抓取簽署者的憑證選項。
ms.assetid: 2362b9d4-d4d8-46fb-8791-7e856827fb31
title: 簽署者. 選項屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.Options
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 7b4a787524e967b5356ed7fb5531a3ec7d7dbfb99d57fc75217a82f220468db7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898834"
---
# <a name="signeroptions-property"></a>簽署者. 選項屬性

\[[ **選項** ] 屬性可用於 [需求] 區段中指定的作業系統。 相反地，請使用 [**CmsSigner 類別**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

**Options** 屬性會設定或抓取簽署者的憑證選項。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```VB
Signer.Options As CAPICOM_CERTIFICATE_INCLUDE_OPTION
```



## <a name="property-value"></a>屬性值

CAPICOM 憑證的值包含指定簽署者憑證選項的 [**\_ \_ \_ 選項**](capicom-certificate-include-option.md) 列舉。 預設值為 [ \_ \_ \_ \_ 除了根以外的 CAPICOM 憑證包含鏈] \_ 。 下表顯示可能的值。



| 值                                                                                                                                                                                                                                                             | 意義                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_INCLUDE_CHAIN_EXCEPT_ROOT"></span><span id="capicom_certificate_include_chain_except_root"></span><dl> <dt>**\_ \_ \_ \_ 除了 \_ 根以外的 CAPICOM 憑證包含鏈**</dt> </dl> | 將所有憑證儲存在鏈中，但根實體除外。<br/> |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_WHOLE_CHAIN"></span><span id="capicom_certificate_include_whole_chain"></span><dl> <dt>**CAPICOM \_ 憑證 \_ 包含 \_ 整個 \_ 鏈**</dt> </dl>                    | 儲存完整的憑證鏈。<br/>                                      |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_END_ENTITY_ONLY"></span><span id="capicom_certificate_include_end_entity_only"></span><dl> <dt>**\_ \_ 僅限 CAPICOM 憑證包含 \_ 結束 \_ 實體 \_**</dt> </dl>       | 只儲存終端實體憑證。<br/>                                     |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**簽署者**](signer.md)
</dt> </dl>

 

 
