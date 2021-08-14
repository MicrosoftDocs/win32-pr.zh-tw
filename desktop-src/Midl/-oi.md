---
title: /Oi 參數
description: /Oi 和/Oic 參數會將 MIDL 編譯器導向，以使用完整解讀的封送處理方法。 /Oicf 參數可提供額外的效能增強功能。
ms.assetid: cf597a45-410f-4098-850b-240c6ebce23b
keywords:
- /Oi 參數 MIDL
topic_type:
- apiref
api_name:
- /Oi
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f38b6faee202e15b7c551297678ce301cbfdcb853b48ecd15c75dda7bb281e72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118385282"
---
# <a name="oi-switch"></a>/Oi 參數

**/Oi** 和 **/Oic** 參數會將 MIDL 編譯器導向，以使用完整解讀的封送處理方法。 **/Oicf** 參數可提供額外的效能增強功能。

``` syntax
midl /{Oi | Oic | Oif | Oicf}
```

## <a name="switch-options"></a>切換選項

<dl> <dt>

*Oi* 
</dt> <dd>

針對在用戶端與伺服器之間傳遞的 stub 程式碼，指定完整解釋的方法。

> [!Note]  
> 此參數已淘汰。 建議您在其位置使用 **/Oicf** 參數。

 

</dd> <dt>

*Oic* 
</dt> <dd>

指定封送處理的無程式碼 proxy 方法，提供 **/Oi** 的所有功能，同時也可進一步減少物件介面的用戶端 stub 程式碼大小。

> [!Note]  
> 此參數已淘汰。 建議您在其位置使用 **/Oicf** 參數。

 

</dd> <dt>

*Oif 或 Oicf* 
</dt> <dd>

指定封送處理的無程式碼 proxy 方法，其中包含 **/Oi** 和 **/Oic** 提供的所有功能，但使用新的解譯器 (快速格式字串，) 提供比 **/Oi** 或 **/Oic** 更好的效能。 此參數包含最近的 RPC 增強功能，建議用於新式 RPC 案例。

</dd> </dl>

## <a name="remarks"></a>備註

請注意與支援平臺相關的限制。

MIDL 3.0 編譯器提供兩種方法來封送處理常式代碼：完全解讀的 ( **/Oi**、 **/Oic** 和 **/Oicf**) 和混合模式 ( [**/os**](-os.md)) 。 從 MIDL 版本6.0.359 開始，MIDL 編譯器預設會產生 **/Oicf** 的 [**/robust**](-robust.md) 存根。 某些模式不支援某些語言功能。 在此情況下，編譯器會自動切換至適當的模式，併發出警告。

如果有問題，混合模式 ( [**/os**](-os.md)) 方法可能是最好的方法。 在此模式中，編譯器會選擇封送處理產生的存根中內嵌的一些參數。 雖然這會產生較大的存根大小，但它可提供更高的效能。

完全解讀的方法會完全離線地封送處理資料。 這可大幅減少存根程式碼的大小，但會導致效能降低。 此外，使用完整解釋的方法時，每個程式都有16個參數的限制。 任何包含16個以上參數的程式，將會自動以 [**/os**](-os.md) 模式處理。 **/Oicf** 可提供最佳的效能，而 **/Oi** 則提供最佳的回溯相容性。

如果您的應用程式使用 midl 3.0 所引進的 midl 功能（例如， \[ [**網路 \_ 封送**](wire-marshal.md)處理 \] 和 \[ [**使用者 \_ 封送**](user-marshal.md)處理屬性），您可能會想要使用/Oif 選項 \] 。 如果您的應用程式使用 [管道](/windows/desktop/Rpc/pipes) ，則必須使用 **/Oif** 選項;如果您指定另一個模式，MIDL 編譯器將切換至 **/Oif**。

為了微調存根程式碼的封送處理方式，Microsoft RPC 提供 ACF \[ [**optimize**](optimize.md) \] 屬性。 這個屬性是用來做為介面屬性或 operation 屬性，以選取個別介面或個別作業的封送處理模式。

### <a name="calling-conventions"></a>呼叫慣例

在使用 **/Oi**、 **/Oic** 或 **/Oif** 參數的解讀方法中，MIDL 編譯器所產生的存根，在 C 編譯期間必須編譯為 stdcall 或 cdecl 程式。 PASCAL 或 Fastcall 呼叫慣例將無法運作。 此外，伺服器 stub 必須編譯為 stdcall。

## <a name="examples"></a>範例

**midl/Oi 檔案名 .idl**

**midl/Oic 檔案名 .idl**

**midl/Oif 檔案名 .idl**

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**/robust**](-robust.md)
</dt> <dt>

[**/no \_ 健全**](-no-robust.md)
</dt> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Os**](-os.md)
</dt> <dt>

[**優化**](optimize.md)
</dt> <dt>

[**/no \_ 格式 \_ 選擇**](-no-format-opt.md)
</dt> </dl>

 

 