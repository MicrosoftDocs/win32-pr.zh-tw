---
description: 提供壓縮圖片的圖片層級參數以進行 HEVC 影片解碼。
ms.assetid: F73AE9CD-5BBC-4A9F-8D05-707AD5E2E92A
title: 'DXVA_PicParams_HEVC 結構 (Dxva .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXVA_PicParams_HEVC
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: cafcbf31a7d4b7fee84e6c695f1d0f0a1e0302ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111781"
---
# <a name="dxva_picparams_hevc-structure"></a><span data-ttu-id="a4b71-103">DXVA \_ PicParams \_ HEVC 結構</span><span class="sxs-lookup"><span data-stu-id="a4b71-103">DXVA\_PicParams\_HEVC structure</span></span>

<span data-ttu-id="a4b71-104">提供壓縮圖片的圖片層級參數以進行 HEVC 影片解碼。</span><span class="sxs-lookup"><span data-stu-id="a4b71-104">Provides the picture-level parameters of a compressed picture for HEVC video decoding.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4b71-105">語法</span><span class="sxs-lookup"><span data-stu-id="a4b71-105">Syntax</span></span>


```C++
typedef struct _DXVA_PicParams_HEVC {
  USHORT             PicWidthInMinCbsY;
  USHORT             PicHeightInMinCbsY;
  union {
    struct {
      USHORT chroma_format_idc  :2;
      USHORT separate_colour_plane_flag   :1;
      USHORT bit_depth_luma_minus8   :3;
      USHORT bit_depth_chroma_minus8  :3;
      USHORT log2_max_pic_order_cnt_lsb_minus4  :4;
      USHORT NoPicReorderingFlag   :1;
      USHORT  NoBiPredFlag   :1;
      USHORT ReservedBits1     :1;
    };
    USHORT  wFormatAndSequenceInfoFlags;
  };
  DXVA_PicEntry_HEVC CurrPic;
  UCHAR              sps_max_dec_pic_buffering_minus1;
  UCHAR              log2_min_luma_coding_block_size_minus3;
  UCHAR              log2_diff_max_min_luma_coding_block_size;
  UCHAR              log2_min_transform_block_size_minus2;
  UCHAR              log2_diff_max_min_transform_block_size;
  UCHAR              max_transform_hierarchy_depth_inter;
  UCHAR              max_transform_hierarchy_depth_intra;
  UCHAR              num_short_term_ref_pic_sets;
  UCHAR              num_long_term_ref_pics_sps;
  UCHAR              num_ref_idx_l0_default_active_minus1;
  UCHAR              num_ref_idx_l1_default_active_minus1;
  CHAR               init_qp_minus26;
  UCHAR              ucNumDeltaPocsOfRefRpsIdx;
  USHORT             wNumBitsForShortTermRPSInSlice;
  USHORT             ReservedBits2;
  union {
    struct {
      UINT32 scaling_list_enabled_flag  :1;
      UINT32 amp_enabled_flag  :1;
      UINT32 sample_adaptive_offset_enabled_flag  :1;
      UINT32 pcm_enabled_flag   :1;
      UINT32 pcm_sample_bit_depth_luma_minus1   :4;
      UINT32 pcm_sample_bit_depth_chroma_minus1     :4;
      UINT32 log2_min_pcm_luma_coding_block_size_minus3    :2;
      UINT32 log2_diff_max_min_pcm_luma_coding_block_size  :2;
      UINT32 pcm_loop_filter_disabled_flag  :1;
      UINT32 long_term_ref_pics_present_flag   :1;
      UINT32 sps_temporal_mvp_enabled_flag  :1;
      UINT32 strong_intra_smoothing_enabled_flag   :1;
      UINT32 dependent_slice_segments_enabled_flag    :1;
      UINT32 output_flag_present_flag   :1;
      UINT32 num_extra_slice_header_bits    :3;
      UINT32 sign_data_hiding_enabled_flag  :1;
      UINT32 cabac_init_present_flag  :1;
      UINT32 ReservedBits3    :5;
    };
    UINT32             dwCodingParamToolFlags;
    union {
      struct {
        UINT32 constrained_intra_pred_flag  :1;
        UINT32 transform_skip_enabled_flag  :1;
        UINT32 cu_qp_delta_enabled_flag  :1;
        UINT32 pps_slice_chroma_qp_offsets_present_flag  :1;
        UINT32 weighted_pred_flag  :1;
        UINT32 weighted_bipred_flag  :1;
        UINT32 transquant_bypass_enabled_flag  :1;
        UINT32 tiles_enabled_flag   :1;
        UINT32 entropy_coding_sync_enabled_flag   :1;
        UINT32 uniform_spacing_flag    :1;
        UINT32 loop_filter_across_tiles_enabled_flag   :1;
        UINT32 pps_loop_filter_across_slices_enabled_flag  :1;
        UINT32 deblocking_filter_override_enabled_flag  :1;
        UINT32 pps_deblocking_filter_disabled_flag  :1;
        UINT32 lists_modification_present_flag  :1;
        UINT32 slice_segment_header_extension_present_flag  :1;
        UINT32 IrapPicFlag  :1;
        UINT32 IdrPicFlag     :1;
        UINT32 IntraPicFlag   :1;
        UINT32 ReservedBits4     :13;
      };
      UINT32   dwCodingSettingPicturePropertyFlags;
    };
    CHAR               pps_cb_qp_offset;
    CHAR               pps_cr_qp_offset;
    UCHAR              num_tile_columns_minus1;
    UCHAR              num_tile_rows_minus1;
    USHORT             column_width_minus1[19];
    USHORT             row_height_minus1[21];
    UCHAR              diff_cu_qp_delta_depth;
    CHAR               pps_beta_offset_div2;
    CHAR               pps_tc_offset_div2;
    UCHAR              log2_parallel_merge_level_minus2;
    INT                CurrPicOrderCntVal;
    DXVA_PicEntry_HEVC RefPicList[15];
    UCHAR              ReservedBits5;
    INT                PicOrderCntValList[15];
    UCHAR              RefPicSetStCurrBefore[8];
    UCHAR              RefPicSetStCurrAfter[8];
    UCHAR              RefPicSetLtCurr[8];
    USHORT             ReservedBits6;
    USHORT             ReservedBits7;
    UINT               StatusReportFeedbackNumber;
  };
} DXVA_PicParams_HEVC, *PDXVA_PicParams_HEVC;
```



## <a name="members"></a><span data-ttu-id="a4b71-106">成員</span><span class="sxs-lookup"><span data-stu-id="a4b71-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a4b71-107">**PicWidthInMinCbsY**</span><span class="sxs-lookup"><span data-stu-id="a4b71-107">**PicWidthInMinCbsY**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-108">**PicHeightInMinCbsY**</span><span class="sxs-lookup"><span data-stu-id="a4b71-108">**PicHeightInMinCbsY**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-109">**色度 \_ 格式 \_ idc**</span><span class="sxs-lookup"><span data-stu-id="a4b71-109">**chroma\_format\_idc**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-110">**個別的 \_ 色彩 \_ 平面 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="a4b71-110">**separate\_colour\_plane\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-111">**位 \_ 深度 \_ luma \_ minus8**</span><span class="sxs-lookup"><span data-stu-id="a4b71-111">**bit\_depth\_luma\_minus8**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-112">**位 \_ 深度 \_ 色度 \_ minus8**</span><span class="sxs-lookup"><span data-stu-id="a4b71-112">**bit\_depth\_chroma\_minus8**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-113">**log2 \_ 最大的 \_ pic \_ 訂單 \_ cnt \_ lsb \_ minus4**</span><span class="sxs-lookup"><span data-stu-id="a4b71-113">**log2\_max\_pic\_order\_cnt\_lsb\_minus4**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-114">**NoPicReorderingFlag**</span><span class="sxs-lookup"><span data-stu-id="a4b71-114">**NoPicReorderingFlag**</span></span> 
</dt> <dd></dd> <dt>

 <span data-ttu-id="a4b71-115">**NoBiPredFlag**</span><span class="sxs-lookup"><span data-stu-id="a4b71-115">**NoBiPredFlag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-116">**ReservedBits1**</span><span class="sxs-lookup"><span data-stu-id="a4b71-116">**ReservedBits1**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-117">**wFormatAndSequenceInfoFlags**</span><span class="sxs-lookup"><span data-stu-id="a4b71-117">**wFormatAndSequenceInfoFlags**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-118">**CurrPic**</span><span class="sxs-lookup"><span data-stu-id="a4b71-118">**CurrPic**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-119">**sps \_ 最大 \_ dec 的 \_ pic \_ 緩衝 \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="a4b71-119">**sps\_max\_dec\_pic\_buffering\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-120">**log2 \_ min \_ luma 程式 \_ 代碼 \_ 區塊 \_ 大小 \_ minus3**</span><span class="sxs-lookup"><span data-stu-id="a4b71-120">**log2\_min\_luma\_coding\_block\_size\_minus3**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-121">**log2 \_ diff \_ 最 \_ 小 \_ luma \_ 編碼 \_ 區塊 \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="a4b71-121">**log2\_diff\_max\_min\_luma\_coding\_block\_size**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-122">**log2 \_ min \_ transform \_ block \_ size \_ minus2**</span><span class="sxs-lookup"><span data-stu-id="a4b71-122">**log2\_min\_transform\_block\_size\_minus2**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-123">**log2 \_ 差異 \_ 最大 \_ 最小 \_ 轉換 \_ 區塊 \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="a4b71-123">**log2\_diff\_max\_min\_transform\_block\_size**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-124">**最大 \_ 轉換階層 \_ \_ 深度 \_ 間**</span><span class="sxs-lookup"><span data-stu-id="a4b71-124">**max\_transform\_hierarchy\_depth\_inter**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-125">**最大 \_ 轉換階層 \_ \_ 深度 \_**</span><span class="sxs-lookup"><span data-stu-id="a4b71-125">**max\_transform\_hierarchy\_depth\_intra**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-126">**\_短期 \_ \_ 參考 \_ pic \_ 組**</span><span class="sxs-lookup"><span data-stu-id="a4b71-126">**num\_short\_term\_ref\_pic\_sets**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-127">**\_長 \_ 詞彙 \_ 參考 \_ 圖片 \_ sps**</span><span class="sxs-lookup"><span data-stu-id="a4b71-127">**num\_long\_term\_ref\_pics\_sps**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-128">**num \_ ref \_ idx \_ l0 \_ 預設使用中 \_ \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="a4b71-128">**num\_ref\_idx\_l0\_default\_active\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-129">**num \_ ref \_ idx \_ l1 \_ 預設使用中 \_ \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="a4b71-129">**num\_ref\_idx\_l1\_default\_active\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-130">**init \_ qp \_ minus26**</span><span class="sxs-lookup"><span data-stu-id="a4b71-130">**init\_qp\_minus26**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-131">**ucNumDeltaPocsOfRefRpsIdx**</span><span class="sxs-lookup"><span data-stu-id="a4b71-131">**ucNumDeltaPocsOfRefRpsIdx**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-132">**wNumBitsForShortTermRPSInSlice**</span><span class="sxs-lookup"><span data-stu-id="a4b71-132">**wNumBitsForShortTermRPSInSlice**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-133">**ReservedBits2**</span><span class="sxs-lookup"><span data-stu-id="a4b71-133">**ReservedBits2**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-134">**調整 \_ 清單 \_ 啟用 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="a4b71-134">**scaling\_list\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-135">**amp \_ 啟用 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="a4b71-135">**amp\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-136">**範例調適型 \_ \_ 位移 \_ 已啟用 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="a4b71-136">**sample\_adaptive\_offset\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-137">**pcm \_ 啟用 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="a4b71-137">**pcm\_enabled\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-138">**pcm \_ 範例 \_ 位 \_ 深度 \_ luma \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="a4b71-138">**pcm\_sample\_bit\_depth\_luma\_minus1**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-139">**pcm \_ 範例 \_ 位 \_ 深度 \_ 色度 \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="a4b71-139">**pcm\_sample\_bit\_depth\_chroma\_minus1**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-140">**log2 \_ min \_ pcm \_ luma \_ 編碼 \_ 區塊 \_ 大小 \_ minus3**</span><span class="sxs-lookup"><span data-stu-id="a4b71-140">**log2\_min\_pcm\_luma\_coding\_block\_size\_minus3**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-141">**log2 \_ diff \_ 最 \_ 小 \_ pcm \_ luma \_ 編碼 \_ 區塊 \_ 大小上限**</span><span class="sxs-lookup"><span data-stu-id="a4b71-141">**log2\_diff\_max\_min\_pcm\_luma\_coding\_block\_size**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-142">**pcm \_ 迴圈 \_ 篩選 \_ 停用 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="a4b71-142">**pcm\_loop\_filter\_disabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-143">**長期 \_ \_ 參考 \_ 圖片目前 \_ 的 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="a4b71-143">**long\_term\_ref\_pics\_present\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-144">**sps \_ 時態性 \_ mvp \_ 啟用 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="a4b71-144">**sps\_temporal\_mvp\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-145">**強 \_ 式 \_ \_ 啟用平滑啟用 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="a4b71-145">**strong\_intra\_smoothing\_enabled\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-146">**相依 \_ 磁區 \_ 區段 \_ 已啟用 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="a4b71-146">**dependent\_slice\_segments\_enabled\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-147">**輸出 \_ 旗標 \_ 目前的 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="a4b71-147">**output\_flag\_present\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-148">**\_額外的 \_ 磁區 \_ 標頭 \_ 位**</span><span class="sxs-lookup"><span data-stu-id="a4b71-148">**num\_extra\_slice\_header\_bits**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-149">**簽署 \_ 資料 \_ 隱藏 \_ 啟用 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="a4b71-149">**sign\_data\_hiding\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-150">**cabac \_ init \_ 存在 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="a4b71-150">**cabac\_init\_present\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-151">**ReservedBits3**</span><span class="sxs-lookup"><span data-stu-id="a4b71-151">**ReservedBits3**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-152">**dwCodingParamToolFlags**</span><span class="sxs-lookup"><span data-stu-id="a4b71-152">**dwCodingParamToolFlags**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-153">**受限的 \_ 內部 \_ pred \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="a4b71-153">**constrained\_intra\_pred\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-154">**轉換 \_ 略過 \_ 啟用 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="a4b71-154">**transform\_skip\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-155">**cu \_ qp \_ delta \_ enabled \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="a4b71-155">**cu\_qp\_delta\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-156">**pps \_ 配 \_ \_ 量色度 \_ qp \_ 有 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="a4b71-156">**pps\_slice\_chroma\_qp\_offsets\_present\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-157">**加權 \_ pred \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="a4b71-157">**weighted\_pred\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-158">**加權 \_ bipred \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="a4b71-158">**weighted\_bipred\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-159">**transquant \_ 略過 \_ 啟用 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="a4b71-159">**transquant\_bypass\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-160">**磚 \_ 已啟用 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="a4b71-160">**tiles\_enabled\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-161">**\_ \_ 已啟用熵編碼同步 \_ \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="a4b71-161">**entropy\_coding\_sync\_enabled\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-162">**統一 \_ 間距 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="a4b71-162">**uniform\_spacing\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-163">**\_ \_ 跨 \_ 磚 \_ 啟用 \_ 旗標的迴圈篩選**</span><span class="sxs-lookup"><span data-stu-id="a4b71-163">**loop\_filter\_across\_tiles\_enabled\_flag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-164">**\_跨配 \_ 量 \_ \_ \_ 啟用 \_ 旗標的 pps 迴圈篩選**</span><span class="sxs-lookup"><span data-stu-id="a4b71-164">**pps\_loop\_filter\_across\_slices\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-165">**deblocking \_ 篩選覆 \_ 寫 \_ 啟用 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="a4b71-165">**deblocking\_filter\_override\_enabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-166">**pps \_ deblocking \_ 濾波器 \_ disabled \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="a4b71-166">**pps\_deblocking\_filter\_disabled\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-167">**列出 \_ 修改 \_ 目前的 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="a4b71-167">**lists\_modification\_present\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-168">**配量 \_ 區段 \_ 標題 \_ 延伸 \_ 顯示 \_ 旗標**</span><span class="sxs-lookup"><span data-stu-id="a4b71-168">**slice\_segment\_header\_extension\_present\_flag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-169">**IrapPicFlag**</span><span class="sxs-lookup"><span data-stu-id="a4b71-169">**IrapPicFlag**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-170">**IdrPicFlag**</span><span class="sxs-lookup"><span data-stu-id="a4b71-170">**IdrPicFlag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-171">**IntraPicFlag**</span><span class="sxs-lookup"><span data-stu-id="a4b71-171">**IntraPicFlag**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-172">**ReservedBits4**</span><span class="sxs-lookup"><span data-stu-id="a4b71-172">**ReservedBits4**</span></span> 
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-173">**dwCodingSettingPicturePropertyFlags**</span><span class="sxs-lookup"><span data-stu-id="a4b71-173">**dwCodingSettingPicturePropertyFlags**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-174">**pps \_ cb \_ qp \_ offset**</span><span class="sxs-lookup"><span data-stu-id="a4b71-174">**pps\_cb\_qp\_offset**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-175">**pps \_ cr 的 \_ qp \_ 位移**</span><span class="sxs-lookup"><span data-stu-id="a4b71-175">**pps\_cr\_qp\_offset**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-176">**num \_ 圖格資料 \_ 行 \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="a4b71-176">**num\_tile\_columns\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-177">**並排顯示的資料 \_ \_ 列 \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="a4b71-177">**num\_tile\_rows\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-178">**資料行 \_ 寬度 \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="a4b71-178">**column\_width\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-179">**資料列 \_ 高度 \_ minus1**</span><span class="sxs-lookup"><span data-stu-id="a4b71-179">**row\_height\_minus1**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-180">**diff \_ cu \_ qp \_ delta \_ depth**</span><span class="sxs-lookup"><span data-stu-id="a4b71-180">**diff\_cu\_qp\_delta\_depth**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-181">**pps \_ Beta \_ offset \_ div2**</span><span class="sxs-lookup"><span data-stu-id="a4b71-181">**pps\_beta\_offset\_div2**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-182">**pps \_ tc \_ offset \_ div2**</span><span class="sxs-lookup"><span data-stu-id="a4b71-182">**pps\_tc\_offset\_div2**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-183">**log2 \_ 平行 \_ 合併 \_ 層級 \_ minus2**</span><span class="sxs-lookup"><span data-stu-id="a4b71-183">**log2\_parallel\_merge\_level\_minus2**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-184">**CurrPicOrderCntVal**</span><span class="sxs-lookup"><span data-stu-id="a4b71-184">**CurrPicOrderCntVal**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-185">**RefPicList**</span><span class="sxs-lookup"><span data-stu-id="a4b71-185">**RefPicList**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-186">**ReservedBits5**</span><span class="sxs-lookup"><span data-stu-id="a4b71-186">**ReservedBits5**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-187">**PicOrderCntValList**</span><span class="sxs-lookup"><span data-stu-id="a4b71-187">**PicOrderCntValList**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-188">**RefPicSetStCurrBefore**</span><span class="sxs-lookup"><span data-stu-id="a4b71-188">**RefPicSetStCurrBefore**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-189">**RefPicSetStCurrAfter**</span><span class="sxs-lookup"><span data-stu-id="a4b71-189">**RefPicSetStCurrAfter**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-190">**RefPicSetLtCurr**</span><span class="sxs-lookup"><span data-stu-id="a4b71-190">**RefPicSetLtCurr**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-191">**ReservedBits6**</span><span class="sxs-lookup"><span data-stu-id="a4b71-191">**ReservedBits6**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-192">**ReservedBits7**</span><span class="sxs-lookup"><span data-stu-id="a4b71-192">**ReservedBits7**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="a4b71-193">**StatusReportFeedbackNumber**</span><span class="sxs-lookup"><span data-stu-id="a4b71-193">**StatusReportFeedbackNumber**</span></span>
<span data-ttu-id="a4b71-194"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="a4b71-194"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="a4b71-195">規格需求</span><span class="sxs-lookup"><span data-stu-id="a4b71-195">Requirements</span></span>



| <span data-ttu-id="a4b71-196">需求</span><span class="sxs-lookup"><span data-stu-id="a4b71-196">Requirement</span></span> | <span data-ttu-id="a4b71-197">值</span><span class="sxs-lookup"><span data-stu-id="a4b71-197">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="a4b71-198">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a4b71-198">Minimum supported client</span></span><br/> | <span data-ttu-id="a4b71-199">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a4b71-199">Windows 8.1 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="a4b71-200">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a4b71-200">Minimum supported server</span></span><br/> | <span data-ttu-id="a4b71-201">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a4b71-201">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="a4b71-202">標頭</span><span class="sxs-lookup"><span data-stu-id="a4b71-202">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4b71-203"><dt>Dxva。h</dt></span><span class="sxs-lookup"><span data-stu-id="a4b71-203"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4b71-204">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a4b71-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4b71-205">媒體基礎結構</span><span class="sxs-lookup"><span data-stu-id="a4b71-205">Media Foundation Structures</span></span>](media-foundation-structures.md)
</dt> </dl>

 

 




