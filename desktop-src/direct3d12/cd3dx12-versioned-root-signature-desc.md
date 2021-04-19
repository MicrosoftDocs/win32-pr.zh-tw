---
title: 'CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC 結構 (D3dx12 .h) '
description: 協助程式結構，可讓您輕鬆地初始化 D3D12 版本的根簽章 \_ \_ \_ \_ DESC 結構。
ms.assetid: 4505C1CE-CAA5-4092-B990-75740A2B194C
keywords:
- CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC 結構
topic_type:
- apiref
api_name:
- CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 695b60fef5aba124ce4e6f2ff729fdb9362c7b2c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106981990"
---
# <a name="cd3dx12_versioned_root_signature_desc-structure"></a>CD3DX12 已建立版本的根簽章 \_ \_ \_ \_ DESC 結構

協助程式結構，可讓您輕鬆地初始化 [**D3D12 版本的根簽章 \_ \_ \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) 結構。

## <a name="syntax"></a>語法


```C++
struct CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC  : public D3D12_VERSIONED_ROOT_SIGNATURE_DESC{
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC();
       explicit CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(const D3D12_VERSIONED_ROOT_SIGNATURE_DESC &o);
       explicit CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(const D3D12_ROOT_SIGNATURE_DESC &o);
       explicit CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(const D3D12_ROOT_SIGNATURE_DESC1 &o);
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(UINT numParameters, const D3D12_ROOT_PARAMETER1* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
       CD3DX12_VERSIONED_ROOT_SIGNATURE_DESC(CD3DX12_DEFAULT);
  void inline Init_1_0(UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
  void static inline Init_1_0(D3D12_VERSIONED_ROOT_SIGNATURE_DESC &desc, UINT numParameters, const D3D12_ROOT_PARAMETER* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
  void inline Init_1_1(UINT numParameters, const D3D12_ROOT_PARAMETER1* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
  void static inline Init_1_1(D3D12_VERSIONED_ROOT_SIGNATURE_DESC &desc, UINT numParameters, const D3D12_ROOT_PARAMETER1* _pParameters, UINT numStaticSamplers = 0, const D3D12_STATIC_SAMPLER_DESC* _pStaticSamplers = NULL, D3D12_ROOT_SIGNATURE_FLAGS flags = D3D12_ROOT_SIGNATURE_FLAG_NONE);
};
```



## <a name="members"></a>成員

<dl> <dt>

**CD3DX12 建立版本的根簽章 \_ \_ \_ \_ DESC ()**
</dt> <dd>

針對 CD3DX12 版本的根簽章 DESC，建立新的、未初始化的實例 \_ \_ \_ \_ 。

</dd> <dt>

**明確 CD3DX12 設定版本的根簽章 \_ \_ \_ \_ desc (const D3D12 已建立版本的根簽章 \_ \_ \_ \_ desc &o)**
</dt> <dd>

建立 CD3DX12 版本根簽章 desc 的新實例 \_ \_ \_ \_ ，並以 [**D3D12 版本的根簽章 \_ \_ \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) 結構的內容進行初始化。

</dd> <dt>

**明確 CD3DX12 設定版本的根簽章 \_ \_ \_ \_ desc (const D3D12 根簽章 \_ \_ \_ desc &o)**
</dt> <dd>

建立 CD3DX12 版本根簽章 desc 的新實例 \_ \_ \_ \_ ，並以 [**D3D12 根簽章 \_ \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc) 結構的內容進行初始化。

</dd> <dt>

**明確 CD3DX12 \_ 版本設定根簽章 \_ \_ \_ DESC (const D3D12 \_ root \_ signature \_ DESC1 &o)**
</dt> <dd>

建立 CD3DX12 版本根簽章 DESC 的新實例 \_ \_ \_ \_ ，並以 [**D3D12 根簽章 \_ \_ \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc1) 結構的內容進行初始化。

</dd> <dt>

**CD3DX12 建立版本的根簽章 \_ \_ \_ \_ DESC (UINT numParameters、const D3D12 \_ ROOT \_ PARAMETER \* \_ PPARAMETERS、UINT numStaticSamplers = 0、CONST D3D12 \_ 靜態 \_ 取樣器 \_ DESC \* \_ PSTATICSAMPLERS = Null、D3D12 根簽章 \_ \_ \_ 旗標旗標 = D3D12 根簽章 \_ 旗標 \_ \_ \_ 無)**
</dt> <dd>

建立 CD3DX12 版本根簽章 DESC 的新實例 \_ \_ ，並 \_ \_ 初始化下列參數：

UINT numParameters

const [**D3D12 \_ 根 \_ 參數**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ 靜態 \_ 取樣器 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = Null

[**D3D12 \_根簽章 \_ \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) 標旗標 = D3D12 根簽章 \_ 旗標 \_ \_ \_ 無

</dd> <dt>

**CD3DX12 建立版本的根簽章 \_ \_ \_ \_ DESC (UINT numParameters、const D3D12 \_ 根 \_ PARAMETER1 \* \_ PPARAMETERS、UINT numStaticSamplers = 0、CONST D3D12 \_ 靜態 \_ 取樣器 \_ DESC \* \_ PSTATICSAMPLERS = Null、D3D12 根簽章 \_ \_ \_ 旗標旗標 = D3D12 根簽章 \_ 旗標 \_ \_ \_ 無)**
</dt> <dd>

建立 CD3DX12 版本根簽章 DESC 的新實例 \_ \_ ，並 \_ \_ 初始化下列參數：

UINT numParameters

const [**D3D12 \_ ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ 靜態 \_ 取樣器 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = Null

[**D3D12 \_根簽章 \_ \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) 標旗標 = D3D12 根簽章 \_ 旗標 \_ \_ \_ 無

</dd> <dt>

**CD3DX12 已建立版本的根簽章 \_ \_ \_ \_ DESC (CD3DX12 \_ 預設)**
</dt> <dd>

建立 CD3DX12 版本根簽章 DESC 的新實例 \_ \_ \_ \_ ，並以預設參數初始化：

UINT numParameters = 0

const [**D3D12 \_ ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters = Null

UINT numStaticSamplers = 0

const [**D3D12 \_ 靜態 \_ 取樣器 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = Null

[**D3D12 \_根簽章 \_ \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) 標旗標 = D3D12 根簽章 \_ 旗標 \_ \_ \_ 無

</dd> <dt>

**內嵌 Init \_ 1 \_ 0 (UINT numParameters、const D3D12 \_ 根 \_ 參數 \* \_ pParameters、UINT numStaticSamplers = 0、const D3D12 \_ 靜態 \_ 取樣器 \_ DESC \* \_ pStaticSamplers = Null、D3D12 根簽章 \_ \_ \_ 旗標旗標 = D3D12 根簽章 \_ 旗標 \_ \_ \_ 無)**
</dt> <dd>

指定初始化下列參數的函式：

UINT numParameters

const [**D3D12 \_ 根 \_ 參數**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ 靜態 \_ 取樣器 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = Null

[**D3D12 \_根簽章 \_ \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) 標旗標 = D3D12 根簽章 \_ 旗標 \_ \_ \_ 無

</dd> <dt>

**靜態內嵌 Init \_ 1 \_ 0 (D3D12 已建立版本的根簽章 \_ \_ \_ \_ DESC &DESC、uint numParameters、CONST D3D12 \_ 根 \_ 參數 \* \_ pParameters、uint numStaticSamplers = 0、CONST D3D12 \_ 靜態 \_ 取樣器 \_ DESC \* \_ pStaticSamplers = Null、D3D12 根簽章 \_ \_ \_ 旗標 = D3D12 根 \_ \_ \_ \_ 簽章旗標無)**
</dt> <dd>

指定初始化下列參數的函式：

[**D3D12 \_已建立版本的根簽章 \_ \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) &desc

UINT numParameters

const [**D3D12 \_ 根 \_ 參數**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ 靜態 \_ 取樣器 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = Null

[**D3D12 \_根簽章 \_ \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) 標旗標 = D3D12 根簽章 \_ 旗標 \_ \_ \_ 無

</dd> <dt>

**內嵌 Init \_ 1 \_ 1 (UINT numParameters、const D3D12 \_ ROOT \_ PARAMETER1 \* \_ pParameters、UINT numStaticSamplers = 0、const D3D12 \_ 靜態 \_ 取樣器 \_ DESC \* \_ pStaticSamplers = Null、D3D12 根簽章 \_ \_ \_ 旗標旗標 = D3D12 根簽章 \_ 旗標 \_ \_ \_ 無)**
</dt> <dd>

指定初始化下列參數的函式：

UINT numParameters

const [**D3D12 \_ ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ 靜態 \_ 取樣器 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = Null

[**D3D12 \_根簽章 \_ \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) 標旗標 = D3D12 根簽章 \_ 旗標 \_ \_ \_ 無

</dd> <dt>

**靜態內嵌 Init \_ 1 \_ 1 (D3D12 已建立版本的根簽章 \_ \_ \_ \_ DESC &DESC、uint numParameters、CONST D3D12 \_ 根 \_ PARAMETER1 \* \_ pParameters、uint numStaticSamplers = 0、CONST D3D12 \_ 靜態 \_ 取樣器 \_ DESC \* \_ pStaticSamplers = Null、D3D12 根簽章 \_ \_ \_ 旗標 = D3D12 根 \_ \_ \_ \_ 簽章旗標無)**
</dt> <dd>

指定初始化下列參數的函式：

[**D3D12 \_已建立版本的根簽章 \_ \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) &desc

UINT numParameters

const [**D3D12 \_ ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) \* \_ pParameters

UINT numStaticSamplers = 0

const [**D3D12 \_ 靜態 \_ 取樣器 \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) \* \_ pStaticSamplers = Null

[**D3D12 \_根簽章 \_ \_ 旗**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) 標旗標 = D3D12 根簽章 \_ 旗標 \_ \_ \_ 無

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx12。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**D3D12 已建立版本的根簽章 \_ \_ \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc)
</dt> <dt>

[D3D12 的 Helper 結構](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





