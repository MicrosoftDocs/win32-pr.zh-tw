---
UID: NE:dwrite.DWRITE_FACTORY_TYPE
title: 'DWRITE_FACTORY_TYPE (DWRITE) '
description: 指定 DirectWrite factory 物件的類型。
tech.root: DirectWrite
ms.date: 11/11/2020
ms.topic: reference
req.header: dwrite.h
req.include-header: dwrite_core.h
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DWRITE_FACTORY_TYPE
- dwrite/DWRITE_FACTORY_TYPE
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- dwrite.h
api_name:
- DWRITE_FACTORY_TYPE
ms.openlocfilehash: 51cfbb274d681bb35b806f49aef13cc4a220ee26
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550303"
---
# <a name="dwrite_factory_type-enumeration-dwriteh"></a>DWRITE_FACTORY_TYPE 列舉 (DWRITE .h) 

指定 DirectWrite factory 物件的類型。

> [!IMPORTANT]
> 此 API 可作為 [DirectWrite](../direct-write-portal.md)DWriteCore 執行的一部分。 DWriteCore 是 DirectWrite 的其中一種形式，可在低至 Windows 8 的 Windows 版本上執行，並讓您自由地跨平台使用。 如需詳細資訊和程式碼範例，請參閱 [DWriteCore 總覽](../dwritecore-overview.md)。

## <a name="syntax"></a>Syntax
```cpp
typedef enum DWRITE_FACTORY_TYPE {
  DWRITE_FACTORY_TYPE_SHARED,
  DWRITE_FACTORY_TYPE_ISOLATED,
  DWRITE_FACTORY_TYPE_ISOLATED2
} ;
```

## <a name="constants"></a>常數

| 名稱 | 描述 |
| ---- |:---- |
| DWRITE_FACTORY_TYPE_SHARED | 指出 DirectWrite factory 是共用的處理站，它允許在多個同進程元件之間重複使用快取的字型資料。 這類工廠也會利用跨進程的字型快取元件，以獲得更好的效能。 |
| DWRITE_FACTORY_TYPE_ISOLATED | 表示 DirectWrite factory 物件已隔離。 從隔離處理站建立的物件不會與其他元件的內部 DirectWrite 狀態互動。 |
| DWRITE_FACTORY_TYPE_ISOLATED2 | 表示已限制 DirectWrite factory 物件。 從受限制的處理站建立的物件不會使用或修改其他處理站所使用的內部狀態或快取資料。 此外，系統字型集合只包含已知字型。|

## <a name="examples"></a>範例

請參閱 [DWriteCore 總覽](../dwritecore-overview.md) 主題和 [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) 範例應用程式。

## <a name="remarks"></a>備註

DirectWrite factory 物件包含其內部狀態的相關資訊，例如字型載入器註冊和快取的字型資料。 在大部分情況下，您應該使用共用處理站物件，因為它允許使用 DirectWrite 的多個元件共用內部 DirectWrite 狀態資訊，進而減少記憶體使用量。 不過，在某些情況下，您可能會想要將元件的影響減少到進程的其餘部分，例如來自不受信任來源的外掛程式，方法是將它與其余的進程元件進行沙箱化並隔離。 在這種情況下，您應該使用沙箱元件的隔離處理站。

受限制的處理站比隔離處理站更受鎖定。 它不會以任何方式與跨進程或持續性的字型快取互動。 此外，從這個 factory 傳回的系統字型集合只包含已知字型。 如果您將 **DWRITE_FACTORY_TYPE_ISOLATED2** 傳遞給早于 DWriteCore 的 DWRITE 版本，則 [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) 會傳回 **E_INVALIDARG**。

## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **最低支援的用戶端** | Windows 10，專案留尼旺島 [Win32 apps] |
| **標頭** | dwrite (包含 dwrite_core .h)  |