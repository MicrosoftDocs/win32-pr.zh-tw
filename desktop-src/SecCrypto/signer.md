---
description: 建立 SignedData 或 SignedCode 物件的簽署者。
ms.assetid: fca6489c-56cf-472f-ac0f-73ba531fa212
title: 簽署者物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4da0f63c64a85290d5b36cad046446a9a0feedcd897869a0df1932ee2532a687
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898510"
---
# <a name="signer-object"></a>簽署者物件

\[**簽署者** 物件可在 [需求] 區段中指定的作業系統中使用。 相反地，請使用 [**CmsSigner 類別**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

**簽署者** 物件會建立 [**SignedData**](signeddata.md)或 [**SignedCode**](signedcode.md)物件的簽署者。 **簽署者** 物件的 [**憑證**](certificate.md)必須具有可用來簽署資料的可用私密金鑰。

## <a name="members"></a>成員

**簽署者** 物件有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**簽署者** 物件具有這些方法。



| 方法                      | 描述                                                       |
|:----------------------------|:------------------------------------------------------------------|
| [**載入**](signer-load.md) | 從指定的 PFX 檔案載入簽署憑證。<br/> |



 

### <a name="properties"></a>屬性

**簽署者** 物件具有這些屬性。



| 屬性                                                                     | 存取類型           | Description                                                                                                                                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AuthenticatedAttributes**](signer-authenticatedattributes.md)<br/> | 唯讀<br/>  | 已驗證之屬性的集合。<br/>                                                                                                                                                                                                                                                                                      |
| [**憑證**](signer-certificate.md)<br/>                         | 讀取/寫入<br/> | 代表資料簽署者之憑證的 [**憑證**](certificate.md) 物件。<br/> 當這個屬性的值是直接或間接重設時，會重設物件的整個 [*狀態*](../secgloss/s-gly.md) 。<br/> 這是預設屬性。<br/> |
| [**鏈**](signer-chain.md)<br/>                                     | 唯讀<br/>  | 簽署者的鏈。<br/>                                                                                                                                                                                                                                                                                                         |
| [**選項**](signer-options.md)<br/>                                 | 讀取/寫入<br/> | 設定或抓取簽署者的憑證選項。<br/>                                                                                                                                                                                                                                                                               |



 

## <a name="remarks"></a>備註

您可以建立 **簽署者** 物件，而且可以安全地進行腳本處理。 **簽署者** 物件的 PROGID 是 CAPICOM。簽署者。2。

**CAPICOM 1。*x*：** **簽署者** 物件的 ProgID 為 CAPICOM。簽署者1。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**加密物件**](cryptography-objects.md)
</dt> </dl>

 

 
