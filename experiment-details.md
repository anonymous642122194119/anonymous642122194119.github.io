# Experiment Details

---

## Efficiency Evaluation

We provide a comparison between **WebNorm** and **AgenticNorm** in efficiency. AgenticNorm incurs much longer training and iteration time (about 19.2 minutes per round) than WebNorm (about 5 minutes), and its throughput is slightly lower because it learns a larger and more comprehensive set of invariants. We acknowledge this difference. However, both the training cost and runtime verification speed remain well within a practical range, and AgenticNorm still sustains **1.2 × 10^5 logs/s**, which is sufficient for real-world deployment and remains faster than neural model-based detectors.


<style>
.comparison-table-container {
  display: flex;
  justify-content: center;
  margin: 40px auto;
  max-width: 85%;
}

.comparison-table {
  width: 100%;
  max-width: 800px;
  border-collapse: collapse;
  font-size: 16px;
  background-color: white;
}

.comparison-table thead tr {
  background-color: #f8f9fa;
  border-bottom: 2px solid #dee2e6;
}

.comparison-table th {
  padding: 16px;
  text-align: left;
  font-weight: 600;
  border: 1px solid #dee2e6;
}

.comparison-table td {
  padding: 14px 16px;
  text-align: left;
  border: 1px solid #dee2e6;
}

.comparison-table tbody tr {
  border-bottom: 1px solid #dee2e6;
}

.comparison-table tbody tr:hover {
  background-color: #f8f9fa;
}
</style>

<div class="comparison-table-container">
  <table class="comparison-table">
    <thead>
      <tr>
        <th>Item</th>
        <th>WebNorm</th>
        <th>Ours</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Invariant Generation Time</td>
        <td>4.3 min</td>
        <td>5.8 min</td>
      </tr>
      <tr>
        <td>One Round Iteration Time</td>
        <td>–</td>
        <td>19.4 min</td>
      </tr>
      <tr>
        <td>Total Training Time</td>
        <td>4.3 min</td>
        <td>199.8 min</td>
      </tr>
      <tr>
        <td>Throughput</td>
        <td>3.2 × 10<sup>5</sup> logs/s</td>
        <td>1.2 × 10<sup>5</sup> logs/s</td>
      </tr>
    </tbody>
  </table>
</div>



Importantly, our **lightweight design** refers to **reduced dependencies** (no source code, no proprietary LLMs, no long-context prompts, no high reasoning requirements), **not** reduced computation time. Even with slightly higher verification cost, AgenticNorm becomes easy to deploy locally, privacy-preserving, and independent of heavy external infrastructure.
