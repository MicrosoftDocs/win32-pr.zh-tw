---
description: 提供雜湊字串的功能。
ms.assetid: 893639c2-57b9-48f6-bf60-a21c3368ffeb
title: HashedData 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b6e54d7d2ca52ceafe500615af4063dfc7310b0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989500"
---
# <a name="hasheddata-object"></a>HashedData 物件

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。 請改用 [**system.string 命名空間中的**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) [**HashAlgorithm 類別**](/previous-versions/windows/)。\]

**HashedData** 物件提供雜湊字串的功能。

## <a name="when-to-use"></a>使用時機

**HashedData** 物件是用來執行下列工作：

-   指定包含要雜湊之資料的內容字串。
-   將指定的雜湊演算法套用至內容字串。

## <a name="members"></a>成員

**HashedData** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**HashedData** 物件有這些方法。



| 方法                          | 描述                                        |
|:--------------------------------|:---------------------------------------------------|
| [**散 列**](hasheddata-hash.md) | 建立指定之字串的雜湊。<br/> |



 

### <a name="properties"></a>屬性

**HashedData** 物件具有這些屬性。



| 屬性                                             | 存取類型           | Description                                                                                                                                                                          |
|:-----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**演算法**](hasheddata-algorithm.md)<br/> | 讀取/寫入<br/> | 設定或抓取所使用的雜湊演算法類型。<br/>                                                                                                                     |
| [**值**](hasheddata-value.md)<br/>         | 唯讀<br/>  | 在成功呼叫 [**Hash**](hasheddata-hash.md) 方法之後，取得雜湊的資料。 雜湊會以十六進位格式傳回。 這是預設屬性。<br/> |



 

## <a name="remarks"></a>備註

若要建立大量資料的雜湊，請呼叫每個資料片段的 [**雜湊**](hasheddata-hash.md) 方法。 在讀取屬性之前，會將每個資料片段的雜湊串連至 [**Value**](hasheddata-value.md) 屬性。 當讀取屬性時，會重設 **Value** 屬性的內容。

您可以建立 **HashedData** 物件，而且可以安全地進行腳本處理。 **HashedData** 物件的 ProgID 是「CAPICOM」。HashedData。 1 "。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
