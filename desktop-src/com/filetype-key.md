---
title: 密碼類型索引鍵
description: GetClassFile 用來比對非複合檔案中各種檔案位元組的模式。
ms.assetid: ced23cdb-c184-43fe-ba37-fe1af8664b66
keywords:
- 類型登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a2e331588b627ee5ce9a9c1b69631f1e8a1dbe4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022014"
---
# <a name="filetype-key"></a>密碼類型索引鍵

[**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile)用來比對非複合檔案中各種檔案位元組的模式。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\FileType
   {CLSID}
      n = offset, cb, mask, value
```

<dl> <dt>

<span id="offset"></span><span id="OFFSET"></span>*抵消*
</dt> <dd>

決定從檔案的開頭或結尾算起開始比較的距離。 如果位移是負值，則比較會從檔案結尾減去位移值開始。 除非在前面加上 "0x"，否則 offset 值是十進位類型。

</dd> <dt>

<span id="cb"></span><span id="CB"></span>*Cb*
</dt> <dd>

表示從開始到檔案結尾的長度（以位元組為單位）。 代表檔案中的位元組範圍。 除非在前面加上 "0x"，否則 *cb* 值是十進位值。

</dd> <dt>

<span id="mask"></span><span id="MASK"></span>*面具*
</dt> <dd>

用於遮罩的二進位值（使用邏輯 AND 運算來執行），以及 *offset* 和 *cb* 指定的位元組範圍。 如果省略此值，則會將位元組設定為所有的位元組。 此值一律為十六進位。

</dd> <dt>

<span id="value"></span><span id="VALUE"></span>*價值*
</dt> <dd>

表示必須符合這種檔案類型之檔案的模式。 此模式可用來從其內容中正確識別已知的檔案格式，而不是由它的副檔名來識別。

</dd> </dl>

## <a name="remarks"></a>備註

[**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile)函式會使用專案來比對非複合檔案中不同檔案位元組的模式。 資料 **類型** 有 CLSID 子機碼，其中每個都有一系列的子機碼 **0**、 **1**、 **2**、 **3**。 這些值包含模式，如果相符的話，就會產生指定的 CLSID。 例如，值為 "0，4，FFFFFFFF，ABCD1234" 表示前4個位元組必須以該順序 ABCD1234。 值為 "-4，4，FEFEFEFE" 表示檔案中的最後四個位元組必須是 FEFEFEFE。 如果其中一種模式相符，則會傳回 CLSID。

**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別** 金鑰組應至 **HKEY \_ 類別 \_ 根金鑰**，此機碼是為了與舊版 COM 相容而保留的。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**<\_ 副檔名>**](-file-extension--key.md)
</dt> <dt>

[**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile)
</dt> </dl>

 

 




