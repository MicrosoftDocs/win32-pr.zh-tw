---
UID: NE:dwrite_core.DWriteCoreCreateFactory
title: 'DWriteCoreCreateFactory (dwrite_core .h) '
description: 建立用於後續建立個別 DWriteCore 物件的 factory 物件。
tech.root: DirectWrite
ms.date: 04/21/2021
ms.topic: reference
req.header: dwrite_core.h
req.include-header: ''
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
- DWriteCoreCreateFactory
- dwrite_core/DWriteCoreCreateFactory
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- dwrite_core.h
api_name:
- DWriteCoreCreateFactory
ms.openlocfilehash: 43e43e00385e10f0da0ba459cdc16e84562b72ec
ms.sourcegitcommit: 7024106e3420607420bb04c3f88d9bb4827038c8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/25/2021
ms.locfileid: "107955021"
---
# <a name="dwritecorecreatefactory-function-dwrite_coreh"></a>DWriteCoreCreateFactory 函數 (dwrite_core .h) 

建立用於後續建立個別 DWriteCore 物件的 factory 物件。

> [!IMPORTANT]
> 此 API 可作為 [DirectWrite](../direct-write-portal.md)DWriteCore 執行的一部分。 DWriteCore 是 DirectWrite 的其中一種形式，可在低至 Windows 8 的 Windows 版本上執行，並讓您自由地跨平台使用。 如需詳細資訊和程式碼範例，請參閱 [DWriteCore 總覽](/windows/win32/directwrite/dwritecore-overview)。

## <a name="syntax"></a>語法
```cpp
HRESULT DWRITE_EXPORT DWriteCoreCreateFactory(
    _In_ DWRITE_FACTORY_TYPE factoryType,
    _In_ REFIID iid,
    _COM_Outptr_ IUnknown** factory
);
```

## <a name="parameters"></a>參數

`factoryType`

類型： <b> <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_factory_type">DWRITE_FACTORY_TYPE</a></b>

值，這個值會指定是否要共用、隔離或限制 factory 物件。

`iid`

類型： <b>REFIID</b>

識別 DirectWrite factory 介面的 GUID 值，例如 __uuidof (<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>) 。

`factory`

類型： <b>IUnknown * *</b>

新建立之 DirectWrite factory 物件的指標位址。

## <a name="return-value"></a>傳回值

類型： <b>HRESULT</b>

如果這個方法成功，它會傳回 <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>。 否則，它會傳回 <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> 錯誤碼。

## <a name="examples"></a>範例

請參閱 [DWriteCore 總覽](/windows/win32/directwrite/dwritecore-overview) 主題和 [DWriteCoreGallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) 範例應用程式。

## <a name="remarks"></a>備註

其功能與系統版本 DirectWrite 所匯出的 [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) 函式相同。 DWriteCore 函式有不同的名稱，以避免混淆。

## <a name="requirements"></a>規格需求
| &nbsp; | &nbsp; |
| ---- |:---- |
| **最低支援的用戶端** | Windows 10，專案留尼旺島 [Win32 apps] |
| **標頭** | dwrite (包含 dwrite_core .h)  |
