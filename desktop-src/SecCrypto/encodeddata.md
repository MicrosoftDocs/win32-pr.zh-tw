---
description: 表示 asn.1 編碼資料的區塊。
ms.assetid: af7acc5f-da0a-4235-8496-05db94664ea5
title: EncodedData 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncodedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ba17056aaf2b038abb519c1eff230f6cccb396edea1ee9c1f96077d572e63fe5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874858"
---
# <a name="encodeddata-object"></a>EncodedData 物件

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista 和 Windows XP。 請改用 [**system.string 命名空間中的**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) [**AsnEncodedData 類別**](/dotnet/api/system.security.cryptography.asnencodeddata?view=netcore-3.1)。\]

**EncodedData** 物件代表一組 asn.1 編碼的資料。

## <a name="when-to-use"></a>使用時機

**EncodedData** 物件是由數個 CAPICOM 物件屬性所傳回。 傳回時，這個物件會用來執行下列工作：

-   取得編碼資料的字串表示。
-   取得與編碼資料相關聯的解碼器物件（如果存在的話）。
-   決定編碼資料的類型。

## <a name="members"></a>成員

**EncodedData** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**EncodedData** 物件有這些方法。



| 方法                                 | 描述                                                     |
|:---------------------------------------|:----------------------------------------------------------------|
| [**解碼 器**](encodeddata-decoder.md) | 取得解碼器物件（如果有的話）。<br/>             |
| [**格式**](encodeddata-format.md)   | 傳回編碼資料的字串表示。<br/> |



 

### <a name="properties"></a>屬性

**EncodedData** 物件具有這些屬性。



| 屬性                                      | 存取類型          | 描述                                                          |
|:----------------------------------------------|:---------------------|:---------------------------------------------------------------------|
| [**值**](encodeddata-value.md)<br/> | 唯讀<br/> | 抓取編碼的資料。 這是預設屬性。<br/> |



 

## <a name="remarks"></a>備註

唯一支援的編碼資料類型是 [**CertificatePolicies**](certificatepolicies.md)。

無法建立 **EncodedData** 物件。

下列的 CAPICOM 物件屬性會傳回 **EncodedData** 物件：

-   **PublicKey. EncodedKey**
-   **PublicKey. EncodedParameters**
-   **EncodedData**
-   **EncodedData**

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
