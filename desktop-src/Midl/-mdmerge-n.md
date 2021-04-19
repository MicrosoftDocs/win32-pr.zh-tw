---
title: /n 參數
description: /N 參數會指定撰寫中繼資料檔案的組合深度。
ms.assetid: 7A1F8A9E-B3CC-4BB2-BF50-5662D4560280
keywords:
- /n 參數 MIDL
topic_type:
- apiref
api_name:
- /n
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78197c0f79c6bbe21ae4eb883620b95e6f0bd4c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993619"
---
# <a name="n-switch"></a>/n 參數

**/N** 參數會指定撰寫中繼資料檔案的組合深度。

``` syntax
mdmerge /n namespace_depth
```

## <a name="switch-options"></a>切換選項

<dl> <dt>

*命名空間 \_ 深度* 
</dt> <dd>

指定要組成單一中繼資料檔案的命名空間深度。

</dd> </dl>

## <a name="remarks"></a>備註

以下是您可以使用 **/n** 參數指定的可能值格式。



| 值格式                   | Description                                                                     |
|--------------------------------|---------------------------------------------------------------------------------|
| Int32 > 0                   | 在參數中指定的命名空間深度撰寫所有類型。               |
| -1                             | 將所有類型撰寫為每個命名空間一個 IDL 檔案。                              |
| <namespace>： Int32 > 0 | 在參數中指定的深度，撰寫具有相符命名空間的所有類型。 |
| <namespace>：-1           | 使用相符的命名空間，將所有類型組成每個命名空間的一個檔案。          |



 

下表顯示使用這些命名空間的不同 **/n** 參數組合的結果。

-   Iiterable<t>。
-   DirectUI. Button （控制項）
-   DirectUI （ListView）
-   PlayTo. Target （應用程式）
-   Web.config。 RSS



| 交換器                         | 結果                                                                                                                                                                                                                                                       | 說明                                                                                                                                                                                                                                                                                                                        |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **/n：-1**  /**n：1**               | Windows.winmd                                                                                                                                                                                                                                                | 最後一個/n 參數會覆寫所有先前的-n 參數。                                                                                                                                                                                                                                                                           |
| **/n：-1/n： Windows。 UI：2**         | <dl> <dt>Windows</dt> <dt>. winmd.</dt> <dt>...</dt> .。 </dl> | <dl> <dt>**Windows Foundation** 一律是在-n:2. 上撰寫</dt> <dt>**Windows. UI** 類型為群組。</dt> <dt>**Web.config** 的組成 n:-1。</dt> </dl>       |
| **/n： 1/n： DirectUI：3** | <dl> <dt>Windows.Foundation.winmd</dt> <dt>Windows.UI.DirectUI.winmd </dt> <dt>Windows.winmd</dt> </dl>       | <dl> <dt>**Windows Foundation** 一律是在-n:2. 上撰寫</dt> <dt>**DirectUI** 是在層級3撰寫。</dt> <dt>所有其他類型都是在層級1上組成。</dt> </dl> |



 

以下是處理 **/n** 參數之多個實例的規則。

-   最特定的實例准。 例如，如果您指定 **– n:A.B.C：4– n:A.B： 5**，MDMERGE 會在第4層解析 .c，因為 b. c 比 A.B. 更明確 B. f. 會在深度5中解析，因為它符合 A B 但未 A.B.C。
-   最後一個實例准。 例如，如果您指定 **– n:5 – n:2**，則類型會在層級2組成。
-   這兩個規則都適用。 如果您指定– n:A.B.C：4– n:A.B.C：1，namespace A. C 會由層級1組成。

## <a name="examples"></a>範例

**mdmerge.exe 中繼資料 \_ dir $ (SDK \_ 中繼資料 \_ 路徑) -i $ (內部 \_ SDK \_ 中繼資料 \_ 路徑) -o $ (OBJ \_ 路徑) \\ $O \\ SystemMetadata-v-n:-1-n:Windows.Foundation：2**

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|--------------------------------|
| 用戶端<br/> | Windows 8<br/>           |
| 伺服器<br/> | Windows Server 2012<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> </dl>

 

 





