---
description: X 檔案格式、載入和儲存選項。
ms.assetid: 813a2b4b-6577-4cdf-a2e6-e06870638354
title: D3DXF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d286ad4cf64133683de026893beb9fa081899e6b170e4b3adb478798eb4b3edf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118096073"
---
# <a name="d3dxf"></a>D3DXF

X 檔案格式、載入和儲存選項。

## <a name="file-formats"></a>檔案格式

下表指定檔資料的類型：



| \#定義檔案格式     | 值 | 描述                                                                                    |
|-------------------------------|-------|------------------------------------------------------------------------------------------------|
| D3DXF \_ >fileformat \_ 二進位檔     | 0     | 舊版格式的二進位檔案。 請參閱 [X 檔案參考 (舊版) ](dx9-graphics-reference-x-file.md)。 |
| D3DXF \_ >fileformat \_ 文字       | 1     | 文字檔。                                                                                     |
| D3DXF \_ >fileformat \_ 壓縮 | 2     | 壓縮檔案。 使用這個旗標時，您也必須指定二進位格式或文字格式。   |



 

## <a name="file-load-options"></a>檔案載入選項

下表指定副檔名為 x 的檔案載入選項：



| \#定義                      | 值 | 描述                |
|-------------------------------|-------|----------------------------|
| D3DXF \_ FILELOAD \_ FromFile     | 0     | 從檔案載入資料。     |
| D3DXF \_ FILELOAD \_ FROMWFILE    | 1     | 從檔案載入資料。     |
| D3DXF \_ FILELOAD \_ FROMRESOURCE | 2     | 從資源載入資料。 |
| D3DXF \_ FILELOAD \_ FROMMEMORY   | 3     | 從記憶體載入資料。     |



 

## <a name="file-save-options"></a>檔儲存選項

下表指定 file save 和 load 選項與. x 檔案：



| \#定義                 | 值 | 描述                    |
|--------------------------|-------|--------------------------------|
| D3DXF \_ FILESAVE \_ TOFILE  | 0     | 儲存至檔案。                |
| D3DXF \_ FILESAVE \_ TOWFILE | 1     | 儲存至寬字元的檔案。 |



 

## <a name="constant-information"></a>常數資訊



| 需求                         | 值           |
|--------------------------|------------|
| 標頭                   | d3dx9xof。h |
| 最低作業系統 | Windows 98 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[D3DX X 檔案常數](dx9-graphics-reference-d3dx-x-file-constants.md)
</dt> <dt>

[**D3DXSaveMeshToX**](d3dxsavemeshtox.md)
</dt> </dl>

 

 



