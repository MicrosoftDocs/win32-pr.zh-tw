---
description: 提供屬性和方法來建立要以數位簽章簽署的內容、以數位方式簽署或 cosign 資料，以及驗證已簽署資料的數位簽章。 簽署的訊息是 PKCS \# 7 格式。
ms.assetid: 500437e8-a637-4e89-9ac9-aa3ea20d437f
title: SignedData 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6d0424826f7dc5d041b877ced1cd7f50490d7801
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994590"
---
# <a name="signeddata-object"></a>SignedData 物件

\[**SignedData** 物件可用於 [需求] 區段中指定的作業系統。 相反地，請使用 [**SignedCms 類別**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

**SignedData** 物件提供屬性和方法來建立要以 [*數位簽章*](../secgloss/d-gly.md)簽署的內容、以數位方式簽署或 cosign 資料，以及驗證已簽署資料的數位簽章。 簽署的訊息是 PKCS \# 7 格式。

如果資料簽章經過驗證，就會證明簽署者與資料之間的關聯性，並顯示資料在建立簽章之後不會以任何方式變更。

## <a name="members"></a>成員

**SignedData** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**SignedData** 物件有這些方法。



| 方法                              | 描述                                                         |
|:------------------------------------|:--------------------------------------------------------------------|
| [**CoSign**](signeddata-cosign.md) | Cosigns 已簽署的訊息。<br/>                       |
| [**標誌**](signeddata-sign.md)     | 在要簽署的內容上建立數位簽章。<br/> |
| [**驗證**](signeddata-verify.md) | 判斷簽章或簽章的有效性。<br/>    |



 

### <a name="properties"></a>屬性

**SignedData** 物件具有這些屬性。



| 屬性                                                   | 存取類型           | Description                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:-----------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**憑證**](signeddata-certificates.md)<br/> | 唯讀<br/>  | 抓取已簽署資料的 [**憑證**](certificates.md) 集合。<br/>                                                                                                                                                                                                                                                                                                                                                          |
| [**內容**](signeddata-content.md)<br/>           | 讀取/寫入<br/> | 要簽署的資料。 這個屬性必須在呼叫 [**Sign**](signeddata-sign.md) 方法之前初始化。<br/> 當這個屬性的值是直接或間接重設時，會重設物件的整個 [*狀態*](../secgloss/s-gly.md) ，而且在變更屬性之前與物件相關聯的任何簽章都會遺失。<br/> 這是預設屬性。<br/> |
| [**簽名**](signeddata-signers.md)<br/>           | 唯讀<br/>  | 抓取代表資料簽章建立者的 [**簽署**](signers.md) 者集合。<br/>                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>備註

您可以建立 **SignedData** 物件，而且可以安全地進行腳本處理。 **SignedData** 物件的 PROGID 是 CAPICOM。SignedData。1。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**加密物件**](cryptography-objects.md)
</dt> </dl>

 

 
