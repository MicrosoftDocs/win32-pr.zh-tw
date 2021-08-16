---
title: /pack 參數
description: /Pack 參數與/Zp 選項相同。
ms.assetid: 381e3099-adb4-4219-bbb4-89c9e1dd3928
keywords:
- /pack 參數 MIDL
topic_type:
- apiref
api_name:
- /pack
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad9282cd5ab56d2e037ba585676a83c5cd558ecb26354ab191899ad341506f5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117991940"
---
# <a name="pack-switch"></a>/pack 參數

**/Pack** 參數與 [**/Zp**](-zp.md)選項相同。

``` syntax
midl /pack packing_level
```

## <a name="switch-options"></a>切換選項

<dl> <dt>

*封裝 \_ 層級* 
</dt> <dd>

指定目標系統中結構的封裝層級。 封裝層級值可以設定為1、2、4或8。

</dd> </dl>

## <a name="remarks"></a>備註

**/Pack** 參數會指定目標系統中結構的封裝層級。 封裝層級值會對應到 Microsoft C/c + + 7.0 版編譯器所使用的 [**/Zp**](-zp.md) 選項值。 如需詳細資訊，請參閱 Microsoft C/c + + 程式設計檔。

當您叫用 MIDL 編譯器和 C 編譯器時，請指定相同的封裝層級。 未指定 [**/Zp**](-zp.md) 或 **/pack** 參數時，所使用的預設封裝層級在這兩個組建環境中都是8。

如需使用非標準封裝層級的潛在危險討論，請參閱 [**/Zp**](-zp.md) 說明主題。

## <a name="examples"></a>範例

**midl/pack 2 檔案名 .idl**

**midl/pack 8 bar .idl**

## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> <dt>

[**/env**](-env.md)
</dt> <dt>

[**/Zp**](-zp.md)
</dt> </dl>

 

 




