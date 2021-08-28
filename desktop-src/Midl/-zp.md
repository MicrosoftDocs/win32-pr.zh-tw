---
title: /Zp 參數
description: /Zp 參數與/pack 選項相同。
ms.assetid: ccdae6a5-e53c-4ddc-9f5f-2b2118709fdb
keywords:
- /Zp 參數 MIDL
topic_type:
- apiref
api_name:
- /Zp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1795068aae1a5a8c3e793b828d5a80dbab369e16f9c5383af367b66d0febc738
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067438"
---
# <a name="zp-switch"></a>/Zp 參數

**/Zp** 參數與 [**/pack**](-pack.md)選項相同。

``` syntax
midl /Zp packing_level
```

## <a name="switch-options"></a>切換選項

<dl> <dt>

*封裝 \_ 層級* 
</dt> <dd>

指定目標系統中結構的封裝層級。 封裝層級值可以設定為1、2、4或8。

</dd> </dl>

## <a name="remarks"></a>備註

**/Zp** 參數會指定目標系統中結構的封裝層級。 封裝層級值會對應到 Microsoft C/c + + 編譯器所使用的 **/Zp** 選項值。 如需詳細資訊，請參閱 Microsoft C/c + + 程式設計檔。

當您叫用 MIDL 編譯器和 C 編譯器時，請指定相同的封裝層級。

未指定 **/Zp** 或 [**/pack**](-pack.md) 參數時，所使用的預設封裝層級在所有組建環境中都是8。

> [!Note]  
> 請勿在 MIPS 或 Alpha 平臺上使用 **/Zp1** 或 **/Zp2** ，而且在16位平臺上請勿使用 **/Zp4** 或 **了/zp8** 。 視 C 編譯器在執行時間所指派的資料類型和記憶體位置而定，這可能會導致 MIPS 和 Alpha 平臺上發生資料不一致的例外狀況。 在 MS-DOS 平臺上，C 編譯器不會確定對齊4或8，因此應用程式可能會終止。

 

## <a name="examples"></a>範例

**midl/Zp4 檔案名 .idl**

## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> <dt>

[**/pack**](-pack.md)
</dt> </dl>

 

 




