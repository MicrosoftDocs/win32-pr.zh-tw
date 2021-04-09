---
description: ID3DX10ThreadPump 介面用來以非同步方式載入資料的資料載入物件。
ms.assetid: bda2414c-bbab-47ac-b23a-f58fb86e732d
title: 'ID3DX10DataLoader 介面 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataLoader
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b0e45d24d663f0ba9a8978bc251a4adf0c7868fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946112"
---
# <a name="id3dx10dataloader-interface"></a>ID3DX10DataLoader 介面

[**ID3DX10ThreadPump 介面**](id3dx10threadpump.md)用來以非同步方式載入資料的資料載入物件。

## <a name="members"></a>成員

**ID3DX10DataLoader** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **ID3DX10DataLoader** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DX10DataLoader** 介面具有這些方法。



| 方法                                             | 描述                                                                                                                                                                                                                        |
|:---------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**解 壓縮**](id3dx10dataloader-decompress.md) | 用來解壓縮編碼的資料。 這通常是用來從檔案系統（例如 ZIP 檔案）載入資源。 從未壓縮的資源載入時，解壓縮階段不需要執行任何工作。<br/> |
| [**摧毀**](id3dx10dataloader-destroy.md)       | 在工作專案完成後， [**ID3DX10ThreadPump 介面**](id3dx10threadpump.md) 用來終結載入器。<br/>                                                                                                   |
| [**載入**](id3dx10dataloader-load.md)             | 由 [**ID3DX10ThreadPump 介面**](id3dx10threadpump.md) 用來從磁片載入資料。<br/>                                                                                                                            |



 

## <a name="remarks"></a>備註

可以繼承這個物件，並重新定義其成員。 這麼做可讓您自訂 API 以載入和解壓縮您自己的自訂檔案格式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 介面](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
