---
title: 'ID3DX11DataLoader 介面 (D3DX11core .h) '
description: 請注意，D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，而且不支援 Windows Store 應用程式。 ID3DX11ThreadPump 介面用來以非同步方式載入資料的資料載入物件。
ms.assetid: 878929ea-0228-4650-9ca0-f83d60d9f915
keywords:
- ID3DX11DataLoader 介面 Direct3D 11
- ID3DX11DataLoader 介面 Direct3D 11，描述
topic_type:
- apiref
api_name:
- ID3DX11DataLoader
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92b688fcbeff21edf23f6a3be1b39be5a9cf0000
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471644"
---
# <a name="id3dx11dataloader-interface"></a>ID3DX11DataLoader 介面

> [!Note]  
> D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，不支援 Windows Store 應用程式。

 

[**ID3DX11ThreadPump 介面**](id3dx11threadpump.md)用來以非同步方式載入資料的資料載入物件。

## <a name="members"></a>成員

**ID3DX11DataLoader** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **ID3DX11DataLoader** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DX11DataLoader** 介面具有這些方法。




| 方法 | 描述 | 
|--------|-------------|
| <a href="id3dx11dataloader-decompress.md"><strong>解 壓縮</strong></a> | <blockquote>[!Note]<br />D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，不支援 Windows Store 應用程式。</blockquote><br /> 解壓縮編碼的資料。<br /> | 
| <a href="id3dx11dataloader-destroy.md"><strong>摧毀</strong></a> | <blockquote>[!Note]<br />D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，不支援 Windows Store 應用程式。</blockquote><br /> 在工作專案完成後終結載入器。<br /> | 
| <a href="id3dx11dataloader-load.md"><strong>載入</strong></a> | <blockquote>[!Note]<br />D3DX (D3DX 9、D3DX 10 和 D3DX 11) 公用程式庫已針對 Windows 8 淘汰，不支援 Windows Store 應用程式。</blockquote><br /> 從磁片載入資料。<br /> | 




 

## <a name="remarks"></a>備註

可以繼承這個物件，並重新定義其成員。 這麼做可讓您自訂 API 以載入和解壓縮您自己的自訂檔案格式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                              |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>D3DX11core。h</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>D3DX11 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 介面](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

